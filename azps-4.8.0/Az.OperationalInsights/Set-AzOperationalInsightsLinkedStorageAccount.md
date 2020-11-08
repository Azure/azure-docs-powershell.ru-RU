---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242947"
---
# <span data-ttu-id="2467e-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2467e-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2467e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2467e-102">SYNOPSIS</span></span>
<span data-ttu-id="2467e-103">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="2467e-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2467e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2467e-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2467e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2467e-105">DESCRIPTION</span></span>
<span data-ttu-id="2467e-106">Настройка связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="2467e-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="2467e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2467e-107">EXAMPLES</span></span>

### <span data-ttu-id="2467e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2467e-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="2467e-109">Задание связанного хранилища для рабочей области</span><span class="sxs-lookup"><span data-stu-id="2467e-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="2467e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2467e-110">PARAMETERS</span></span>

### <span data-ttu-id="2467e-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2467e-111">-DataSourceType</span></span>
<span data-ttu-id="2467e-112">Тип источника данных должен быть "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="2467e-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="2467e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2467e-113">-DefaultProfile</span></span>
<span data-ttu-id="2467e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2467e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2467e-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2467e-115">-Force</span></span>
<span data-ttu-id="2467e-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="2467e-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2467e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2467e-117">-ResourceGroupName</span></span>
<span data-ttu-id="2467e-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2467e-118">The resource group name.</span></span>

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

### <span data-ttu-id="2467e-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="2467e-119">-StorageAccountIds</span></span>
<span data-ttu-id="2467e-120">список идентификаторов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2467e-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="2467e-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2467e-121">-WorkspaceName</span></span>
<span data-ttu-id="2467e-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2467e-122">The workspace name.</span></span>

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

### <span data-ttu-id="2467e-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2467e-123">-Confirm</span></span>
<span data-ttu-id="2467e-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2467e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2467e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2467e-125">-WhatIf</span></span>
<span data-ttu-id="2467e-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2467e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2467e-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2467e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2467e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2467e-128">CommonParameters</span></span>
<span data-ttu-id="2467e-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2467e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2467e-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2467e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2467e-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2467e-131">INPUTS</span></span>

### <span data-ttu-id="2467e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2467e-132">System.String</span></span>

## <span data-ttu-id="2467e-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2467e-133">OUTPUTS</span></span>

### <span data-ttu-id="2467e-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="2467e-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="2467e-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2467e-135">NOTES</span></span>

## <span data-ttu-id="2467e-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2467e-136">RELATED LINKS</span></span>
