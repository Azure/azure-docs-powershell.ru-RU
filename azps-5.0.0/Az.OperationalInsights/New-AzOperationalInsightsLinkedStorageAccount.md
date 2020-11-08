---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248081"
---
# <span data-ttu-id="5921f-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5921f-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="5921f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5921f-102">SYNOPSIS</span></span>
<span data-ttu-id="5921f-103">Создание связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="5921f-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="5921f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5921f-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5921f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5921f-105">DESCRIPTION</span></span>
<span data-ttu-id="5921f-106">Создание связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="5921f-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="5921f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5921f-107">EXAMPLES</span></span>

### <span data-ttu-id="5921f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5921f-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="5921f-109">Добавление связанного хранилища для рабочей области</span><span class="sxs-lookup"><span data-stu-id="5921f-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="5921f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5921f-110">PARAMETERS</span></span>

### <span data-ttu-id="5921f-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="5921f-111">-DataSourceType</span></span>
<span data-ttu-id="5921f-112">Тип источника данных должен быть "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="5921f-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="5921f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5921f-113">-DefaultProfile</span></span>
<span data-ttu-id="5921f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5921f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5921f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5921f-115">-Force</span></span>
<span data-ttu-id="5921f-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="5921f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="5921f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5921f-117">-ResourceGroupName</span></span>
<span data-ttu-id="5921f-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5921f-118">The resource group name.</span></span>

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

### <span data-ttu-id="5921f-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="5921f-119">-StorageAccountIds</span></span>
<span data-ttu-id="5921f-120">список идентификаторов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="5921f-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="5921f-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5921f-121">-WorkspaceName</span></span>
<span data-ttu-id="5921f-122">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5921f-122">The workspace name.</span></span>

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

### <span data-ttu-id="5921f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5921f-123">-Confirm</span></span>
<span data-ttu-id="5921f-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5921f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5921f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5921f-125">-WhatIf</span></span>
<span data-ttu-id="5921f-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5921f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5921f-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5921f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5921f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5921f-128">CommonParameters</span></span>
<span data-ttu-id="5921f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5921f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5921f-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5921f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5921f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5921f-131">INPUTS</span></span>

### <span data-ttu-id="5921f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="5921f-132">System.String</span></span>

## <span data-ttu-id="5921f-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5921f-133">OUTPUTS</span></span>

### <span data-ttu-id="5921f-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="5921f-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="5921f-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5921f-135">NOTES</span></span>

## <span data-ttu-id="5921f-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5921f-136">RELATED LINKS</span></span>
