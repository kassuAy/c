# code
class Solution:
    def kClosest(self, points: List[List[int]], k: int) -> List[List[int]]:
        minHeap=[]
        for x,y in points:
            distination=(x**2)+(y**2)
            minHeap.append([distination,x,y])
        heapq.heapify(minHeap)
        result=[]
        while k>0:
            distination,x,y=heapq.heappop(minHeap)
            result.append([x,y])
            k-=1
        return result
        
