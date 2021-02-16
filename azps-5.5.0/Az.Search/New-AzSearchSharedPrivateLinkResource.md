---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 1a9f76ef0d1955076171cc157686b7ae5d7be266
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226761"
---
# <span data-ttu-id="188af-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="188af-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="188af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="188af-102">SYNOPSIS</span></span>
<span data-ttu-id="188af-103">Создает ресурс общей частной ссылки для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="188af-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="188af-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="188af-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="188af-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="188af-105">DESCRIPTION</span></span>
<span data-ttu-id="188af-106">Новая **служба AzSearchSharedPrivateLinkResource** создает ресурс общей частной ссылки для службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="188af-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="188af-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="188af-107">EXAMPLES</span></span>

### <span data-ttu-id="188af-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="188af-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="188af-109">В этом примере создается общий личный ресурс ссылки на службу BLOB-хранилищ учетной записи службы azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="188af-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="188af-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="188af-110">PARAMETERS</span></span>

### <span data-ttu-id="188af-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="188af-111">-AsJob</span></span>
<span data-ttu-id="188af-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="188af-112">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="188af-113">-DefaultProfile</span></span>
<span data-ttu-id="188af-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="188af-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="188af-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="188af-115">-GroupId</span></span>
<span data-ttu-id="188af-116">Shared private link resource id</span><span class="sxs-lookup"><span data-stu-id="188af-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-117">-Name</span><span class="sxs-lookup"><span data-stu-id="188af-117">-Name</span></span>
<span data-ttu-id="188af-118">Ресурс личной ссылки "Общий поиск" в Azure Cognitive Search</span><span class="sxs-lookup"><span data-stu-id="188af-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="188af-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="188af-120">Shared private link target resource id</span><span class="sxs-lookup"><span data-stu-id="188af-120">Shared private link target resource id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="188af-121">-RequestMessage</span></span>
<span data-ttu-id="188af-122">Сообщение с запросом ресурсов на доступную личную ссылку</span><span class="sxs-lookup"><span data-stu-id="188af-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="188af-123">-ResourceGroupName</span></span>
<span data-ttu-id="188af-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="188af-124">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="188af-125">-ResourceRegion</span></span>
<span data-ttu-id="188af-126">(Необязательно) Область ресурсов общей личной ссылки</span><span class="sxs-lookup"><span data-stu-id="188af-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="188af-127">-ServiceName</span></span>
<span data-ttu-id="188af-128">Имя службы поиска данных Azure.</span><span class="sxs-lookup"><span data-stu-id="188af-128">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="188af-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="188af-129">-Confirm</span></span>
<span data-ttu-id="188af-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="188af-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="188af-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="188af-131">-WhatIf</span></span>
<span data-ttu-id="188af-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="188af-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="188af-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="188af-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="188af-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="188af-134">CommonParameters</span></span>
<span data-ttu-id="188af-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="188af-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="188af-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="188af-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="188af-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="188af-137">INPUTS</span></span>

### <span data-ttu-id="188af-138">Нет</span><span class="sxs-lookup"><span data-stu-id="188af-138">None</span></span>

## <span data-ttu-id="188af-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="188af-139">OUTPUTS</span></span>

### <span data-ttu-id="188af-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="188af-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="188af-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="188af-141">NOTES</span></span>

## <span data-ttu-id="188af-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="188af-142">RELATED LINKS</span></span>

[<span data-ttu-id="188af-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="188af-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="188af-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="188af-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="188af-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="188af-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
