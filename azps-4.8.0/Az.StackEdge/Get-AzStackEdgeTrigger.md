---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94080222"
---
# <span data-ttu-id="5e885-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5e885-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="5e885-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e885-102">SYNOPSIS</span></span>
<span data-ttu-id="5e885-103">Получение триггеров, настроенных на устройстве</span><span class="sxs-lookup"><span data-stu-id="5e885-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="5e885-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e885-104">SYNTAX</span></span>

### <span data-ttu-id="5e885-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e885-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e885-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e885-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e885-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e885-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e885-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e885-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="5e885-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e885-109">DESCRIPTION</span></span>
<span data-ttu-id="5e885-110">Командлет **Get-AzStackEdgeTriger** получает триггеры для устройства.</span><span class="sxs-lookup"><span data-stu-id="5e885-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="5e885-111">Вы можете указать имя в качестве параметра в командлете, чтобы получить подробные сведения о конкретных триггерах.</span><span class="sxs-lookup"><span data-stu-id="5e885-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="5e885-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e885-112">EXAMPLES</span></span>

### <span data-ttu-id="5e885-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5e885-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="5e885-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e885-114">PARAMETERS</span></span>

### <span data-ttu-id="5e885-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e885-115">-DefaultProfile</span></span>
<span data-ttu-id="5e885-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e885-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e885-117">-Имя_устройства</span><span class="sxs-lookup"><span data-stu-id="5e885-117">-DeviceName</span></span>
<span data-ttu-id="5e885-118">Имя устройства</span><span class="sxs-lookup"><span data-stu-id="5e885-118">Device Name</span></span>

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

### <span data-ttu-id="5e885-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="5e885-119">-DeviceObject</span></span>
<span data-ttu-id="5e885-120">Укажите соответствующий объект устройства</span><span class="sxs-lookup"><span data-stu-id="5e885-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="5e885-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5e885-121">-Name</span></span>
<span data-ttu-id="5e885-122">Название ресурса</span><span class="sxs-lookup"><span data-stu-id="5e885-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e885-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e885-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e885-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5e885-124">Resource Group Name</span></span>

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

### <span data-ttu-id="5e885-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e885-125">-ResourceId</span></span>
<span data-ttu-id="5e885-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e885-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="5e885-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e885-127">CommonParameters</span></span>
<span data-ttu-id="5e885-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e885-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e885-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e885-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e885-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e885-130">INPUTS</span></span>

### <span data-ttu-id="5e885-131">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="5e885-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="5e885-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e885-132">OUTPUTS</span></span>

### <span data-ttu-id="5e885-133">Microsoft. Azure. PowerShell. командлеты. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="5e885-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="5e885-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e885-134">NOTES</span></span>

## <span data-ttu-id="5e885-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e885-135">RELATED LINKS</span></span>
