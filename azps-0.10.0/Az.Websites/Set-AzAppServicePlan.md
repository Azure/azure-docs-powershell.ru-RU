---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/set-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Set-AzAppServicePlan.md
ms.openlocfilehash: b679b98e84f389e35e7dc291822049e554d40a9a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910567"
---
# <span data-ttu-id="a1584-101">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a1584-101">Set-AzAppServicePlan</span></span>

## <span data-ttu-id="a1584-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a1584-102">SYNOPSIS</span></span>
<span data-ttu-id="a1584-103">Задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a1584-103">Sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a1584-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a1584-104">SYNTAX</span></span>

### <span data-ttu-id="a1584-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="a1584-105">S1</span></span>
```
Set-AzAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1584-106">S2</span><span class="sxs-lookup"><span data-stu-id="a1584-106">S2</span></span>
```
Set-AzAppServicePlan [-AppServicePlan] <AppServicePlan> [-AsJob]
[-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1584-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1584-107">DESCRIPTION</span></span>
<span data-ttu-id="a1584-108">Командлет **Set-AzAppServicePlan** задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="a1584-108">The **Set-AzAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="a1584-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a1584-109">EXAMPLES</span></span>

### <span data-ttu-id="a1584-110">1: изменение плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a1584-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="a1584-111">Эта команда устанавливает для параметра PerSiteScaling значение true для плана служб приложений с именем ContosoASP, который принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a1584-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a1584-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a1584-112">PARAMETERS</span></span>

### <span data-ttu-id="a1584-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="a1584-113">-AdminSiteName</span></span>
<span data-ttu-id="a1584-114">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="a1584-114">Admin Site Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a1584-115">-AppServicePlan</span></span>
<span data-ttu-id="a1584-116">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a1584-116">App Service Plan Object</span></span>

```yaml
Type: AppServicePlan
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1584-117">-DefaultProfile</span></span>
<span data-ttu-id="a1584-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1584-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1584-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a1584-119">-Name</span></span>
<span data-ttu-id="a1584-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="a1584-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="a1584-121">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="a1584-121">-NumberofWorkers</span></span>
<span data-ttu-id="a1584-122">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="a1584-122">Number Of Workers</span></span>

```yaml
Type: Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-123">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="a1584-123">-PerSiteScaling</span></span>
<span data-ttu-id="a1584-124">Логическое масштабирование на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="a1584-124">Per Site Scaling Boolean</span></span>

```yaml
Type: Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1584-125">-ResourceGroupName</span></span>
<span data-ttu-id="a1584-126">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a1584-126">Resource Group Name</span></span>

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

### <span data-ttu-id="a1584-127">Уровень</span><span class="sxs-lookup"><span data-stu-id="a1584-127">-Tier</span></span>
<span data-ttu-id="a1584-128">Уровневый</span><span class="sxs-lookup"><span data-stu-id="a1584-128">Tier</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium, PremiumV2

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1584-129">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="a1584-129">-WorkerSize</span></span>
<span data-ttu-id="a1584-130">Размер рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="a1584-130">Worker Size</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="a1584-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a1584-131">-AsJob</span></span>
<span data-ttu-id="a1584-132">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a1584-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a1584-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1584-133">CommonParameters</span></span>
<span data-ttu-id="a1584-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a1584-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1584-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1584-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1584-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a1584-136">INPUTS</span></span>

### <span data-ttu-id="a1584-137">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="a1584-137">ServerFarmWithRichSku</span></span>
<span data-ttu-id="a1584-138">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a1584-138">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="a1584-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1584-139">OUTPUTS</span></span>

### <span data-ttu-id="a1584-140">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="a1584-140">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="a1584-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="a1584-141">NOTES</span></span>

## <span data-ttu-id="a1584-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1584-142">RELATED LINKS</span></span>

[<span data-ttu-id="a1584-143">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-143">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a1584-144">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-144">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a1584-145">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-145">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a1584-146">Restarting-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-146">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a1584-147">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-147">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="a1584-148">Остановить-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a1584-148">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


