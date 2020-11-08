---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: 56179260dc045b83ed067e92c6aa8bd7f880c38c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243838"
---
# <span data-ttu-id="cd100-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cd100-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="cd100-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd100-102">SYNOPSIS</span></span>
<span data-ttu-id="cd100-103">Извлекает доступные роли для устройства.</span><span class="sxs-lookup"><span data-stu-id="cd100-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="cd100-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd100-104">SYNTAX</span></span>

### <span data-ttu-id="cd100-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cd100-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd100-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd100-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd100-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd100-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd100-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cd100-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="cd100-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd100-109">DESCRIPTION</span></span>
<span data-ttu-id="cd100-110">Командлет **Get-AzStackEdgeRole** извлекает доступные роли IOT для краевого устройства стека.</span><span class="sxs-lookup"><span data-stu-id="cd100-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="cd100-111">Вы можете упомянуть о параметре name, чтобы получить сведения о конкретной роли Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cd100-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="cd100-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd100-112">EXAMPLES</span></span>

### <span data-ttu-id="cd100-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cd100-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="cd100-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd100-114">PARAMETERS</span></span>

### <span data-ttu-id="cd100-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd100-115">-DefaultProfile</span></span>
<span data-ttu-id="cd100-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cd100-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="cd100-117">-DeviceName</span></span>
<span data-ttu-id="cd100-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="cd100-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="cd100-119">-DeviceObject</span></span>
<span data-ttu-id="cd100-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="cd100-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cd100-121">-Name</span></span>
<span data-ttu-id="cd100-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="cd100-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd100-123">-ResourceGroupName</span></span>
<span data-ttu-id="cd100-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="cd100-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd100-125">-ResourceId</span></span>
<span data-ttu-id="cd100-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd100-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd100-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd100-127">CommonParameters</span></span>
<span data-ttu-id="cd100-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd100-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd100-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd100-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd100-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd100-130">INPUTS</span></span>

### <span data-ttu-id="cd100-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="cd100-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="cd100-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd100-132">OUTPUTS</span></span>

### <span data-ttu-id="cd100-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="cd100-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="cd100-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd100-134">NOTES</span></span>

## <span data-ttu-id="cd100-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd100-135">RELATED LINKS</span></span>
