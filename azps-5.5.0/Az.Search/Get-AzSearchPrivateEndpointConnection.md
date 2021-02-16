---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242432"
---
# <span data-ttu-id="a7d91-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7d91-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="a7d91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d91-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d91-103">Возвращает частные конечные точки подключения к службе поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d91-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7d91-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a7d91-104">SYNTAX</span></span>

### <span data-ttu-id="a7d91-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a7d91-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7d91-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d91-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7d91-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d91-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d91-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a7d91-108">DESCRIPTION</span></span>
<span data-ttu-id="a7d91-109">С **помощью cmdlet Get-AzSearchPrivateEndpointConnection** можно получить частные конечные точки подключения к службе поиска когнитивных функций Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d91-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7d91-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a7d91-110">EXAMPLES</span></span>

### <span data-ttu-id="a7d91-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a7d91-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="a7d91-112">В этом примере личные подключения конечных точек к службе azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a7d91-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="a7d91-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a7d91-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="a7d91-114">Пример возвращает конкретное подключение частной конечной точки по имени (преобразуется в JSON для у удобства чтения) в службу azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a7d91-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7d91-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7d91-115">PARAMETERS</span></span>

### <span data-ttu-id="a7d91-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d91-116">-DefaultProfile</span></span>
<span data-ttu-id="a7d91-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d91-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d91-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d91-118">-Name</span></span>
<span data-ttu-id="a7d91-119">Имя частного подключения конечной точки службы поиска Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="a7d91-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7d91-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a7d91-120">-ParentObject</span></span>
<span data-ttu-id="a7d91-121">Объект ввода службы поиска Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d91-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d91-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d91-122">-ResourceGroupName</span></span>
<span data-ttu-id="a7d91-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7d91-123">Resource Group name.</span></span>

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

### <span data-ttu-id="a7d91-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7d91-124">-ResourceId</span></span>
<span data-ttu-id="a7d91-125">Private link service resource id</span><span class="sxs-lookup"><span data-stu-id="a7d91-125">Private link service resource id</span></span>

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

### <span data-ttu-id="a7d91-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a7d91-126">-ServiceName</span></span>
<span data-ttu-id="a7d91-127">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="a7d91-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a7d91-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7d91-128">-Confirm</span></span>
<span data-ttu-id="a7d91-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d91-130">-WhatIf</span></span>
<span data-ttu-id="a7d91-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7d91-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7d91-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a7d91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d91-133">CommonParameters</span></span>
<span data-ttu-id="a7d91-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d91-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d91-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d91-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d91-136">INPUTS</span></span>

### <span data-ttu-id="a7d91-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a7d91-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a7d91-138">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d91-138">System.String</span></span>

## <span data-ttu-id="a7d91-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a7d91-139">OUTPUTS</span></span>

### <span data-ttu-id="a7d91-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a7d91-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="a7d91-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a7d91-141">NOTES</span></span>

## <span data-ttu-id="a7d91-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a7d91-142">RELATED LINKS</span></span>

[<span data-ttu-id="a7d91-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a7d91-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="a7d91-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="a7d91-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
