---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/invoke-azrestmethod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Invoke-AzRestMethod.md
ms.openlocfilehash: f8475c7cead6159231314989d21430658128c01f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248161"
---
# <span data-ttu-id="b64e8-101">Invoke-AzRestMethod</span><span class="sxs-lookup"><span data-stu-id="b64e8-101">Invoke-AzRestMethod</span></span>

## <span data-ttu-id="b64e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b64e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b64e8-103">Создание и выполнение запроса HTTP для конечной точки управления ресурсами Azure</span><span class="sxs-lookup"><span data-stu-id="b64e8-103">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="b64e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b64e8-104">SYNTAX</span></span>

### <span data-ttu-id="b64e8-105">ByPath (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b64e8-105">ByPath (Default)</span></span>
```
Invoke-AzRestMethod -Path <String> -Method <String> [-Payload <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b64e8-106">ByParameters</span><span class="sxs-lookup"><span data-stu-id="b64e8-106">ByParameters</span></span>
```
Invoke-AzRestMethod [-SubscriptionId <String>] [-ResourceGroupName <String>] [-ResourceProviderName <String>]
 [-ResourceType <String[]>] [-Name <String[]>] -ApiVersion <String> -Method <String> [-Payload <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b64e8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b64e8-107">DESCRIPTION</span></span>
<span data-ttu-id="b64e8-108">Создание и выполнение запроса HTTP для конечной точки управления ресурсами Azure</span><span class="sxs-lookup"><span data-stu-id="b64e8-108">Construct and perform HTTP request to Azure resource management endpoint only</span></span>

## <span data-ttu-id="b64e8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b64e8-109">EXAMPLES</span></span>

### <span data-ttu-id="b64e8-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b64e8-110">Example 1</span></span>
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

<span data-ttu-id="b64e8-111">Получение рабочей области для службы аналитики журналов по пути</span><span class="sxs-lookup"><span data-stu-id="b64e8-111">Get log analytics workspace by path</span></span>

## <span data-ttu-id="b64e8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b64e8-112">PARAMETERS</span></span>

### <span data-ttu-id="b64e8-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b64e8-113">-ApiVersion</span></span>
<span data-ttu-id="b64e8-114">Версия API</span><span class="sxs-lookup"><span data-stu-id="b64e8-114">Api Version</span></span>

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

### <span data-ttu-id="b64e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b64e8-115">-AsJob</span></span>
<span data-ttu-id="b64e8-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b64e8-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b64e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b64e8-117">-DefaultProfile</span></span>
<span data-ttu-id="b64e8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b64e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b64e8-119">-Method</span><span class="sxs-lookup"><span data-stu-id="b64e8-119">-Method</span></span>
<span data-ttu-id="b64e8-120">Метод HTTP</span><span class="sxs-lookup"><span data-stu-id="b64e8-120">Http Method</span></span>

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

### <span data-ttu-id="b64e8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b64e8-121">-Name</span></span>
<span data-ttu-id="b64e8-122">список имен целевых ресурсов</span><span class="sxs-lookup"><span data-stu-id="b64e8-122">list of Target Resource Name</span></span>

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

### <span data-ttu-id="b64e8-123">-Path</span><span class="sxs-lookup"><span data-stu-id="b64e8-123">-Path</span></span>
<span data-ttu-id="b64e8-124">Целевой путь</span><span class="sxs-lookup"><span data-stu-id="b64e8-124">Target Path</span></span>

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

### <span data-ttu-id="b64e8-125">-Полезные данные</span><span class="sxs-lookup"><span data-stu-id="b64e8-125">-Payload</span></span>
<span data-ttu-id="b64e8-126">Полезные данные в формате JSON</span><span class="sxs-lookup"><span data-stu-id="b64e8-126">JSON format payload</span></span>

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

### <span data-ttu-id="b64e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b64e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="b64e8-128">Имя целевой группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b64e8-128">Target Resource Group Name</span></span>

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

### <span data-ttu-id="b64e8-129">-ResourceProviderName</span><span class="sxs-lookup"><span data-stu-id="b64e8-129">-ResourceProviderName</span></span>
<span data-ttu-id="b64e8-130">Имя целевого поставщика ресурсов</span><span class="sxs-lookup"><span data-stu-id="b64e8-130">Target Resource Provider Name</span></span>

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

### <span data-ttu-id="b64e8-131">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="b64e8-131">-ResourceType</span></span>
<span data-ttu-id="b64e8-132">Список целевых типов ресурсов</span><span class="sxs-lookup"><span data-stu-id="b64e8-132">List of Target Resource Type</span></span>

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

### <span data-ttu-id="b64e8-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b64e8-133">-SubscriptionId</span></span>
<span data-ttu-id="b64e8-134">Идентификатор целевой подписки</span><span class="sxs-lookup"><span data-stu-id="b64e8-134">Target Subscription Id</span></span>

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

### <span data-ttu-id="b64e8-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b64e8-135">-Confirm</span></span>
<span data-ttu-id="b64e8-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b64e8-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b64e8-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b64e8-137">-WhatIf</span></span>
<span data-ttu-id="b64e8-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b64e8-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b64e8-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b64e8-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b64e8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b64e8-140">CommonParameters</span></span>
<span data-ttu-id="b64e8-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b64e8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b64e8-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b64e8-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b64e8-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b64e8-143">INPUTS</span></span>

### <span data-ttu-id="b64e8-144">System. String</span><span class="sxs-lookup"><span data-stu-id="b64e8-144">System.string</span></span>

## <span data-ttu-id="b64e8-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b64e8-145">OUTPUTS</span></span>

### <span data-ttu-id="b64e8-146">Microsoft. Azure. Commands. Profile. Models. PSHttpResponse</span><span class="sxs-lookup"><span data-stu-id="b64e8-146">Microsoft.Azure.Commands.Profile.Models.PSHttpResponse</span></span>

## <span data-ttu-id="b64e8-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="b64e8-147">NOTES</span></span>

## <span data-ttu-id="b64e8-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b64e8-148">RELATED LINKS</span></span>
