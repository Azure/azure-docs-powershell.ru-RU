---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az
ms.assetid: 8F36244D-A4D7-40BB-AC4C-E9AD445549F8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzAppServicePlan.md
ms.openlocfilehash: 040efd4e483825db637345fbd8bcb54a27e8675b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910603"
---
# <span data-ttu-id="61afd-101">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="61afd-101">New-AzAppServicePlan</span></span>

## <span data-ttu-id="61afd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61afd-102">SYNOPSIS</span></span>
<span data-ttu-id="61afd-103">Создает план служб приложений Azure в указанном географическом расположении.</span><span class="sxs-lookup"><span data-stu-id="61afd-103">Creates an Azure App Service plan in a given Geo location.</span></span>

## <span data-ttu-id="61afd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61afd-104">SYNTAX</span></span>

### <span data-ttu-id="61afd-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="61afd-105">S1</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-ResourceGroupName] <String> [-Name] <String> [-AsJob][-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61afd-106">S2</span><span class="sxs-lookup"><span data-stu-id="61afd-106">S2</span></span>
```
New-AzAppServicePlan [-Location] <String> [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [[-AseName] <String>] [[-AseResourceGroupName] <String>] [-PerSiteScaling <Boolean>]
 [-AppServicePlan] <ServerFarmWithRichSku> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61afd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61afd-107">DESCRIPTION</span></span>
<span data-ttu-id="61afd-108">Командлет **New-AzAppServicePlan** создает план служб приложений Azure в определенном географическом расположении с указанным уровнем, размером рабочего процесса и количеством сотрудников.</span><span class="sxs-lookup"><span data-stu-id="61afd-108">The **New-AzAppServicePlan** cmdlet creates an Azure App Service plan in a given Geo location with the specified Tier, worker size, and number of workers.</span></span>

## <span data-ttu-id="61afd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61afd-109">EXAMPLES</span></span>

### <span data-ttu-id="61afd-110">Пример 1: создание плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="61afd-110">Example 1: Create an App Service plan</span></span>
```
PS C:\>New-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -Location "West US" -Tier "Basic" -NumberofWorkers 2 -WorkerSize "Small"
```

<span data-ttu-id="61afd-111">Эта команда создает план служб приложений с именем ContosoASP в группе ресурсов с именем Default-Web-WestUS в географическом расположении Запад US.</span><span class="sxs-lookup"><span data-stu-id="61afd-111">This command creates an App Service plan named ContosoASP in the resource group named Default-Web-WestUS in Geo location West US.</span></span>
<span data-ttu-id="61afd-112">Команда задает базовый уровень и распределяется между двумя маленькими сотрудниками.</span><span class="sxs-lookup"><span data-stu-id="61afd-112">The command specifies a Basic Tier and allocates two small workers.</span></span>

## <span data-ttu-id="61afd-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61afd-113">PARAMETERS</span></span>

### <span data-ttu-id="61afd-114">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="61afd-114">-AppServicePlan</span></span>
<span data-ttu-id="61afd-115">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="61afd-115">App Service Plan Object</span></span>

```yaml
Type: ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-116">-AseName</span><span class="sxs-lookup"><span data-stu-id="61afd-116">-AseName</span></span>
<span data-ttu-id="61afd-117">Имя среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="61afd-117">App Service Environment Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-118">-AseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61afd-118">-AseResourceGroupName</span></span>
<span data-ttu-id="61afd-119">Имя группы ресурсов среды службы приложений</span><span class="sxs-lookup"><span data-stu-id="61afd-119">App Service Environment Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61afd-120">-DefaultProfile</span></span>
<span data-ttu-id="61afd-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61afd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-122">-Location</span><span class="sxs-lookup"><span data-stu-id="61afd-122">-Location</span></span>
<span data-ttu-id="61afd-123">Поиска</span><span class="sxs-lookup"><span data-stu-id="61afd-123">Location</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="61afd-124">-Name</span></span>
<span data-ttu-id="61afd-125">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="61afd-125">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-126">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="61afd-126">-NumberofWorkers</span></span>
<span data-ttu-id="61afd-127">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="61afd-127">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-128">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="61afd-128">-PerSiteScaling</span></span>
<span data-ttu-id="61afd-129">Включение или выключение масштабирования на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="61afd-129">Whether or not to enable Per Site Scaling</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61afd-130">-ResourceGroupName</span></span>
<span data-ttu-id="61afd-131">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="61afd-131">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-132">Уровень</span><span class="sxs-lookup"><span data-stu-id="61afd-132">-Tier</span></span>
<span data-ttu-id="61afd-133">Уровневый</span><span class="sxs-lookup"><span data-stu-id="61afd-133">Tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: Free
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61afd-134">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="61afd-134">-WorkerSize</span></span>
<span data-ttu-id="61afd-135">Размер веб-рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="61afd-135">Size of web worker</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: Small
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="61afd-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61afd-136">-AsJob</span></span>
<span data-ttu-id="61afd-137">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61afd-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61afd-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61afd-138">CommonParameters</span></span>
<span data-ttu-id="61afd-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61afd-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61afd-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61afd-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61afd-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61afd-141">INPUTS</span></span>

### <span data-ttu-id="61afd-142">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="61afd-142">ServerFarmWithRichSku</span></span>
<span data-ttu-id="61afd-143">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="61afd-143">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="61afd-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61afd-144">OUTPUTS</span></span>

### <span data-ttu-id="61afd-145">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="61afd-145">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="61afd-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="61afd-146">NOTES</span></span>

## <span data-ttu-id="61afd-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61afd-147">RELATED LINKS</span></span>

[<span data-ttu-id="61afd-148">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="61afd-148">Get-AzAppServicePlan</span></span>](./Get-AzAppServicePlan.md)

[<span data-ttu-id="61afd-149">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="61afd-149">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="61afd-150">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="61afd-150">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


