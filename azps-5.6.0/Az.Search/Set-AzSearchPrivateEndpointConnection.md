---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: d67108e935d4f3ef14522f792a06f975d98be803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972552"
---
# <span data-ttu-id="11887-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11887-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="11887-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11887-102">SYNOPSIS</span></span>
<span data-ttu-id="11887-103">Обновив подключение закрытой конечной точки к службе поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="11887-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="11887-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="11887-104">SYNTAX</span></span>

### <span data-ttu-id="11887-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11887-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11887-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11887-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11887-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11887-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11887-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11887-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11887-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11887-109">DESCRIPTION</span></span>
<span data-ttu-id="11887-110">**Set-AzSearchPrivateEndpointConnection** обновляет подключение частной конечной точки к службе azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="11887-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="11887-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="11887-111">EXAMPLES</span></span>

### <span data-ttu-id="11887-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11887-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="11887-113">В этом примере состояние частного подключения конечной точки службы azure Cognitive Search обновилось на "Отклонено".</span><span class="sxs-lookup"><span data-stu-id="11887-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="11887-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11887-114">PARAMETERS</span></span>

### <span data-ttu-id="11887-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11887-115">-DefaultProfile</span></span>
<span data-ttu-id="11887-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11887-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11887-117">-Description</span><span class="sxs-lookup"><span data-stu-id="11887-117">-Description</span></span>
<span data-ttu-id="11887-118">Описание подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="11887-118">Private endpoint connection description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11887-119">-InputObject</span></span>
<span data-ttu-id="11887-120">Объект ввода подключения к закрытой конечной точке</span><span class="sxs-lookup"><span data-stu-id="11887-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11887-121">-Name</span><span class="sxs-lookup"><span data-stu-id="11887-121">-Name</span></span>
<span data-ttu-id="11887-122">Имя частного подключения конечной точки службы поиска Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="11887-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="11887-123">-ParentObject</span></span>
<span data-ttu-id="11887-124">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="11887-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11887-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11887-125">-ResourceGroupName</span></span>
<span data-ttu-id="11887-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11887-126">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11887-127">-ResourceId</span></span>
<span data-ttu-id="11887-128">Private link service resource id</span><span class="sxs-lookup"><span data-stu-id="11887-128">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11887-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11887-129">-ServiceName</span></span>
<span data-ttu-id="11887-130">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="11887-130">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-131">-Status</span><span class="sxs-lookup"><span data-stu-id="11887-131">-Status</span></span>
<span data-ttu-id="11887-132">Состояние подключения к закрытой службе ссылок</span><span class="sxs-lookup"><span data-stu-id="11887-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11887-133">-Confirm</span></span>
<span data-ttu-id="11887-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="11887-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11887-135">-WhatIf</span></span>
<span data-ttu-id="11887-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11887-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11887-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="11887-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11887-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11887-138">CommonParameters</span></span>
<span data-ttu-id="11887-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11887-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11887-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11887-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11887-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="11887-141">INPUTS</span></span>

### <span data-ttu-id="11887-142">System.String</span><span class="sxs-lookup"><span data-stu-id="11887-142">System.String</span></span>

## <span data-ttu-id="11887-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11887-143">OUTPUTS</span></span>

### <span data-ttu-id="11887-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="11887-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="11887-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="11887-145">NOTES</span></span>

## <span data-ttu-id="11887-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11887-146">RELATED LINKS</span></span>

[<span data-ttu-id="11887-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="11887-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="11887-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="11887-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
