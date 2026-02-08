local vipWalls = workspace.DefaultMap_SharedInstances:FindFirstChild("VIPWalls")

local function freeAll()
    if vipWalls then
        for _,v in pairs(vipWalls:GetDescendants()) do
            if v:IsA("BasePart") then
                v.CanCollide = false
            end
        end
    end
end

while true do
    freeAll()
    task.wait(1)
end
