---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240400"
---
# <span data-ttu-id="6e854-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6e854-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="6e854-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e854-102">SYNOPSIS</span></span>
<span data-ttu-id="6e854-103">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6e854-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6e854-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6e854-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e854-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e854-105">DESCRIPTION</span></span>
<span data-ttu-id="6e854-106">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6e854-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="6e854-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6e854-107">EXAMPLES</span></span>

### <span data-ttu-id="6e854-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e854-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="6e854-109">Настройка связанного хранилища для рабочей области</span><span class="sxs-lookup"><span data-stu-id="6e854-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="6e854-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e854-110">PARAMETERS</span></span>

### <span data-ttu-id="6e854-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="6e854-111">-DataSourceType</span></span>
<span data-ttu-id="6e854-112">Тип источника данных должен быть одним из типов CustomLogs и AzureWatson.</span><span class="sxs-lookup"><span data-stu-id="6e854-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="6e854-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e854-113">-DefaultProfile</span></span>
<span data-ttu-id="6e854-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6e854-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e854-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6e854-115">-Force</span></span>
<span data-ttu-id="6e854-116">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6e854-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="6e854-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e854-117">-ResourceGroupName</span></span>
<span data-ttu-id="6e854-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6e854-118">The resource group name.</span></span>

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

### <span data-ttu-id="6e854-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="6e854-119">-StorageAccountIds</span></span>
<span data-ttu-id="6e854-120">список ИД учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6e854-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="6e854-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6e854-121">-WorkspaceName</span></span>
<span data-ttu-id="6e854-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="6e854-122">The workspace name.</span></span>

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

### <span data-ttu-id="6e854-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e854-123">-Confirm</span></span>
<span data-ttu-id="6e854-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6e854-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e854-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e854-125">-WhatIf</span></span>
<span data-ttu-id="6e854-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e854-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e854-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6e854-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e854-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e854-128">CommonParameters</span></span>
<span data-ttu-id="6e854-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e854-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e854-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6e854-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e854-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e854-131">INPUTS</span></span>

### <span data-ttu-id="6e854-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6e854-132">System.String</span></span>

## <span data-ttu-id="6e854-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6e854-133">OUTPUTS</span></span>

### <span data-ttu-id="6e854-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="6e854-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="6e854-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6e854-135">NOTES</span></span>

## <span data-ttu-id="6e854-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e854-136">RELATED LINKS</span></span>
