---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1392e77ef6497265dde8bcf0a05a86529253f539
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989722"
---
# <span data-ttu-id="6bb0c-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6bb0c-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6bb0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bb0c-102">SYNOPSIS</span></span>
<span data-ttu-id="6bb0c-103">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6bb0c-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6bb0c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6bb0c-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bb0c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-105">DESCRIPTION</span></span>
<span data-ttu-id="6bb0c-106">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6bb0c-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6bb0c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-107">EXAMPLES</span></span>

### <span data-ttu-id="6bb0c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6bb0c-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="6bb0c-109">Настройка связанного хранилища для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6bb0c-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="6bb0c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bb0c-110">PARAMETERS</span></span>

### <span data-ttu-id="6bb0c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="6bb0c-111">-DataSourceType</span></span>
<span data-ttu-id="6bb0c-112">Тип источника данных должен быть одним из типов CustomLogs и AzureWatson.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bb0c-113">-DefaultProfile</span></span>
<span data-ttu-id="6bb0c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6bb0c-115">-Force</span></span>
<span data-ttu-id="6bb0c-116">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-116">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bb0c-117">-ResourceGroupName</span></span>
<span data-ttu-id="6bb0c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="6bb0c-119">-StorageAccountIds</span></span>
<span data-ttu-id="6bb0c-120">список ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6bb0c-121">-WorkspaceName</span></span>
<span data-ttu-id="6bb0c-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-122">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6bb0c-123">-Confirm</span></span>
<span data-ttu-id="6bb0c-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bb0c-125">-WhatIf</span></span>
<span data-ttu-id="6bb0c-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bb0c-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bb0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bb0c-128">CommonParameters</span></span>
<span data-ttu-id="6bb0c-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bb0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bb0c-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bb0c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bb0c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb0c-131">INPUTS</span></span>

### <span data-ttu-id="6bb0c-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6bb0c-132">System.String</span></span>

## <span data-ttu-id="6bb0c-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6bb0c-133">OUTPUTS</span></span>

### <span data-ttu-id="6bb0c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="6bb0c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="6bb0c-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-135">NOTES</span></span>

## <span data-ttu-id="6bb0c-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6bb0c-136">RELATED LINKS</span></span>
