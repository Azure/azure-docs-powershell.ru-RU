---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 56f9f5b86e3e98ca9bba13604c3086d2189c45c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234846"
---
# <span data-ttu-id="cba8c-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cba8c-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="cba8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cba8c-102">SYNOPSIS</span></span>
<span data-ttu-id="cba8c-103">Удаление связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="cba8c-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="cba8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cba8c-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cba8c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba8c-105">DESCRIPTION</span></span>
<span data-ttu-id="cba8c-106">Удаление связанной учетной записи хранения для рабочей области</span><span class="sxs-lookup"><span data-stu-id="cba8c-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="cba8c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cba8c-107">EXAMPLES</span></span>

### <span data-ttu-id="cba8c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cba8c-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="cba8c-109">Удаление связанной учетной записи хранилища с типом "CustomLogs" для {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="cba8c-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="cba8c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cba8c-110">PARAMETERS</span></span>

### <span data-ttu-id="cba8c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="cba8c-111">-DataSourceType</span></span>
<span data-ttu-id="cba8c-112">Тип источника данных должен быть "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="cba8c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="cba8c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba8c-113">-DefaultProfile</span></span>
<span data-ttu-id="cba8c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cba8c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cba8c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cba8c-115">-Force</span></span>
<span data-ttu-id="cba8c-116">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="cba8c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cba8c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cba8c-117">-ResourceGroupName</span></span>
<span data-ttu-id="cba8c-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cba8c-118">The resource group name.</span></span>

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

### <span data-ttu-id="cba8c-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cba8c-119">-WorkspaceName</span></span>
<span data-ttu-id="cba8c-120">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cba8c-120">The workspace name.</span></span>

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

### <span data-ttu-id="cba8c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cba8c-121">-Confirm</span></span>
<span data-ttu-id="cba8c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cba8c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cba8c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cba8c-123">-WhatIf</span></span>
<span data-ttu-id="cba8c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cba8c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cba8c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cba8c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cba8c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba8c-126">CommonParameters</span></span>
<span data-ttu-id="cba8c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cba8c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba8c-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cba8c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba8c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cba8c-129">INPUTS</span></span>

### <span data-ttu-id="cba8c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cba8c-130">System.String</span></span>

## <span data-ttu-id="cba8c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba8c-131">OUTPUTS</span></span>

### <span data-ttu-id="cba8c-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cba8c-132">System.Boolean</span></span>

## <span data-ttu-id="cba8c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="cba8c-133">NOTES</span></span>

## <span data-ttu-id="cba8c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cba8c-134">RELATED LINKS</span></span>