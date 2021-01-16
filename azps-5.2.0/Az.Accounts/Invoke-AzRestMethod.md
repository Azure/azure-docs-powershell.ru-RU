---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413007"
---
# <span data-ttu-id="1aeb7-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="1aeb7-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="1aeb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aeb7-102">SYNOPSIS</span></span>
<span data-ttu-id="1aeb7-103">Создание и выполнение HTTP-запроса только для конечной точки управления ресурсами Azure</span><span class="sxs-lookup"><span data-stu-id="1aeb7-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="1aeb7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1aeb7-104">SYNTAX</span></span>

### <span data-ttu-id="1aeb7-105">ByPath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1aeb7-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aeb7-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="1aeb7-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aeb7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1aeb7-107">DESCRIPTION</span></span>
<span data-ttu-id="1aeb7-108">Создание и выполнение HTTP-запроса только для конечной точки управления ресурсами Azure</span><span class="sxs-lookup"><span data-stu-id="1aeb7-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="1aeb7-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1aeb7-109">EXAMPLES</span></span>

### <span data-ttu-id="1aeb7-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1aeb7-110">Example 1</span></span>
```powershell
Invoke-AzRestMethod -Path "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}?api-version={API}" -Method GET

Headers    : {[Cache-Control, System.String[]], [Pragma, System.String[]], [x-ms-request-id, System.String[]], [Strict-Transport-Security, System.String[]]…}
Version    : 1.1
StatusCode : 200
Method     : GET
Content    : {
               "properties": {
                 "source": "Azure",
                 "customerId": "{customerId}",
                 "provisioningState": "Succeeded",
                 "sku": {
                   "name": "pergb2018",
                   "maxCapacityReservationLevel": 3000,
                   "lastSkuUpdate": "Mon, 25 May 2020 11:10:01 GMT"
                 },
                 "retentionInDays": 30,
                 "features": {
                   "legacy": 0,
                   "searchVersion": 1,
                   "enableLogAccessUsingOnlyResourcePermissions": true
                 },
                 "workspaceCapping": {
                   "dailyQuotaGb": -1.0,
                   "quotaNextResetTime": "Thu, 18 Jun 2020 05:00:00 GMT",
                   "dataIngestionStatus": "RespectQuota"
                 },
                 "enableFailover": false,
                 "publicNetworkAccessForIngestion": "Enabled",
                 "publicNetworkAccessForQuery": "Enabled",
                 "createdDate": "Mon, 25 May 2020 11:10:01 GMT",
                 "modifiedDate": "Mon, 25 May 2020 11:10:02 GMT"
               },
               "id": "/subscriptions/{subscription}/resourcegroups/{resourcegroup}/providers/microsoft.operationalinsights/workspaces/{workspace}",
               "name": "{workspace}",
               "type": "Microsoft.OperationalInsights/workspaces",
               "location": "eastasia",
               "tags": {}
             }
```

<span data-ttu-id="1aeb7-111">Получить рабочее пространство для аналитики журналов по пути</span><span class="sxs-lookup"><span data-stu-id="1aeb7-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="1aeb7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aeb7-112">PARAMETERS</span></span>

### <span data-ttu-id="1aeb7-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1aeb7-113">-ApiVersion</span></span>
<span data-ttu-id="1aeb7-114">Версия API</span><span class="sxs-lookup"><span data-stu-id="1aeb7-114">Api Version</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1aeb7-115">-AsJob</span></span>
<span data-ttu-id="1aeb7-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1aeb7-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1aeb7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aeb7-117">-DefaultProfile</span></span>
<span data-ttu-id="1aeb7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1aeb7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aeb7-119">-Method</span><span class="sxs-lookup"><span data-stu-id="1aeb7-119">-Method</span></span>
<span data-ttu-id="1aeb7-120">Метод Http</span><span class="sxs-lookup"><span data-stu-id="1aeb7-120">Http Method</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: GET, POST, PUT, PATCH, DELETE

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1aeb7-121">-Name</span></span>
<span data-ttu-id="1aeb7-122">Список имени конечного ресурса</span><span class="sxs-lookup"><span data-stu-id="1aeb7-122">list of Target Resource Name</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-123">-Path</span><span class="sxs-lookup"><span data-stu-id="1aeb7-123">-Path</span></span>
<span data-ttu-id="1aeb7-124">Целевой путь</span><span class="sxs-lookup"><span data-stu-id="1aeb7-124">Target Path</span></span>

```yaml
Type: String
Parameter Sets: ByPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-125">-Payload</span><span class="sxs-lookup"><span data-stu-id="1aeb7-125">-Payload</span></span>
<span data-ttu-id="1aeb7-126">Полезное сотовая нагрузка в формате JSON</span><span class="sxs-lookup"><span data-stu-id="1aeb7-126">JSON format payload</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aeb7-127">-ResourceGroupName</span></span>
<span data-ttu-id="1aeb7-128">Название целевой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="1aeb7-128">Target Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="1aeb7-129">-ResourceProviderName</span></span>
<span data-ttu-id="1aeb7-130">Имя целевого поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="1aeb7-130">Target Resource Provider Name</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1aeb7-131">-ResourceType</span></span>
<span data-ttu-id="1aeb7-132">Список типа конечного ресурса</span><span class="sxs-lookup"><span data-stu-id="1aeb7-132">List of Target Resource Type</span></span>

```yaml
Type: String[]
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1aeb7-133">-SubscriptionId</span></span>
<span data-ttu-id="1aeb7-134">ИД целевой подписки</span><span class="sxs-lookup"><span data-stu-id="1aeb7-134">Target Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: ByParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aeb7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1aeb7-135">-Confirm</span></span>
<span data-ttu-id="1aeb7-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aeb7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aeb7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aeb7-137">-WhatIf</span></span>
<span data-ttu-id="1aeb7-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aeb7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1aeb7-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1aeb7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aeb7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aeb7-140">CommonParameters</span></span>
<span data-ttu-id="1aeb7-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aeb7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aeb7-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aeb7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aeb7-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1aeb7-143">INPUTS</span></span>

### <span data-ttu-id="1aeb7-144">System.string</span><span class="sxs-lookup"><span data-stu-id="1aeb7-144">System.string</span></span>

## <span data-ttu-id="1aeb7-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1aeb7-145">OUTPUTS</span></span>

### <span data-ttu-id="1aeb7-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="1aeb7-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="1aeb7-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1aeb7-147">NOTES</span></span>

## <span data-ttu-id="1aeb7-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1aeb7-148">RELATED LINKS</span></span>
