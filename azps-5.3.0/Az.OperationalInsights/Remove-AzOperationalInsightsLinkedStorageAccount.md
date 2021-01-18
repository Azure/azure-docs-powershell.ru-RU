---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505460"
---
# <span data-ttu-id="d5293-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d5293-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="d5293-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5293-102">SYNOPSIS</span></span>
<span data-ttu-id="d5293-103">Удаление связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="d5293-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d5293-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d5293-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5293-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5293-105">DESCRIPTION</span></span>
<span data-ttu-id="d5293-106">Удаление связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="d5293-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="d5293-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d5293-107">EXAMPLES</span></span>

### <span data-ttu-id="d5293-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d5293-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="d5293-109">Удалить связанную учетную запись хранения с типом CustomLogs для {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="d5293-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="d5293-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5293-110">PARAMETERS</span></span>

### <span data-ttu-id="d5293-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="d5293-111">-DataSourceType</span></span>
<span data-ttu-id="d5293-112">Тип источника данных должен быть одним из типов CustomLogs и AzureWatson.</span><span class="sxs-lookup"><span data-stu-id="d5293-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5293-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5293-113">-DefaultProfile</span></span>
<span data-ttu-id="d5293-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d5293-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5293-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d5293-115">-Force</span></span>
<span data-ttu-id="d5293-116">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="d5293-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="d5293-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5293-117">-ResourceGroupName</span></span>
<span data-ttu-id="d5293-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5293-118">The resource group name.</span></span>

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

### <span data-ttu-id="d5293-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d5293-119">-WorkspaceName</span></span>
<span data-ttu-id="d5293-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="d5293-120">The workspace name.</span></span>

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

### <span data-ttu-id="d5293-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5293-121">-Confirm</span></span>
<span data-ttu-id="d5293-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5293-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5293-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5293-123">-WhatIf</span></span>
<span data-ttu-id="d5293-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5293-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5293-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d5293-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5293-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5293-126">CommonParameters</span></span>
<span data-ttu-id="d5293-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5293-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5293-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5293-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5293-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5293-129">INPUTS</span></span>

### <span data-ttu-id="d5293-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d5293-130">System.String</span></span>

## <span data-ttu-id="d5293-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5293-131">OUTPUTS</span></span>

### <span data-ttu-id="d5293-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d5293-132">System.Boolean</span></span>

## <span data-ttu-id="d5293-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d5293-133">NOTES</span></span>

## <span data-ttu-id="d5293-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5293-134">RELATED LINKS</span></span>
