---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 32D45795-FBCD-4157-BF45-41BD1F61782E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Set-AzureRmAppServicePlan.md
ms.openlocfilehash: 4b6270a6d56b8f210b2f03311bf19bb09950f361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560403"
---
# <span data-ttu-id="7d232-101">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d232-101">Set-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="7d232-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d232-102">SYNOPSIS</span></span>
<span data-ttu-id="7d232-103">Задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7d232-103">Sets an Azure App Service plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d232-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d232-104">SYNTAX</span></span>

### <span data-ttu-id="7d232-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="7d232-105">S1</span></span>
```
Set-AzureRmAppServicePlan [[-AdminSiteName] <String>] [[-Tier] <String>] [[-NumberofWorkers] <Int32>]
 [[-WorkerSize] <String>] [-PerSiteScaling <Boolean>] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d232-106">S2</span><span class="sxs-lookup"><span data-stu-id="7d232-106">S2</span></span>
```
Set-AzureRmAppServicePlan [-AppServicePlan] <ServerFarmWithRichSku> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d232-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d232-107">DESCRIPTION</span></span>
<span data-ttu-id="7d232-108">Командлет **Set-AzureRmAppServicePlan** задает план служб приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7d232-108">The **Set-AzureRmAppServicePlan** cmdlet sets an Azure App Service plan.</span></span>

## <span data-ttu-id="7d232-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d232-109">EXAMPLES</span></span>

### <span data-ttu-id="7d232-110">1: изменение плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="7d232-110">1: Modify an App Service plan</span></span>
```
PS C:\>Set-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP" -PerSiteScaling $true
```

<span data-ttu-id="7d232-111">Эта команда устанавливает для параметра PerSiteScaling значение true для плана служб приложений с именем ContosoASP, который принадлежит группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="7d232-111">This command sets the PerSiteScaling option to true on the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="7d232-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d232-112">PARAMETERS</span></span>

### <span data-ttu-id="7d232-113">-AdminSiteName</span><span class="sxs-lookup"><span data-stu-id="7d232-113">-AdminSiteName</span></span>
<span data-ttu-id="7d232-114">Имя сайта администратора</span><span class="sxs-lookup"><span data-stu-id="7d232-114">Admin Site Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-115">-AppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d232-115">-AppServicePlan</span></span>
<span data-ttu-id="7d232-116">Объект плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="7d232-116">App Service Plan Object</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d232-117">-Name</span></span>
<span data-ttu-id="7d232-118">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="7d232-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-119">-NumberofWorkers</span><span class="sxs-lookup"><span data-stu-id="7d232-119">-NumberofWorkers</span></span>
<span data-ttu-id="7d232-120">Количество сотрудников</span><span class="sxs-lookup"><span data-stu-id="7d232-120">Number Of Workers</span></span>

```yaml
Type: System.Int32
Parameter Sets: S1
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-121">-PerSiteScaling</span><span class="sxs-lookup"><span data-stu-id="7d232-121">-PerSiteScaling</span></span>
<span data-ttu-id="7d232-122">Логическое масштабирование на уровне сайта</span><span class="sxs-lookup"><span data-stu-id="7d232-122">Per Site Scaling Boolean</span></span>

```yaml
Type: System.Boolean
Parameter Sets: S1
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d232-123">-ResourceGroupName</span></span>
<span data-ttu-id="7d232-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d232-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-125">Уровень</span><span class="sxs-lookup"><span data-stu-id="7d232-125">-Tier</span></span>
<span data-ttu-id="7d232-126">Уровневый</span><span class="sxs-lookup"><span data-stu-id="7d232-126">Tier</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Free, Shared, Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-127">-WorkerSize</span><span class="sxs-lookup"><span data-stu-id="7d232-127">-WorkerSize</span></span>
<span data-ttu-id="7d232-128">Размер рабочего процесса</span><span class="sxs-lookup"><span data-stu-id="7d232-128">Worker Size</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 
Accepted values: Small, Medium, Large, ExtraLarge

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d232-129">-DefaultProfile</span></span>
<span data-ttu-id="7d232-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d232-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d232-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d232-131">CommonParameters</span></span>
<span data-ttu-id="7d232-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d232-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d232-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d232-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d232-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d232-134">INPUTS</span></span>

### <span data-ttu-id="7d232-135">ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7d232-135">ServerFarmWithRichSku</span></span>
<span data-ttu-id="7d232-136">Параметр "AppServicePlan" принимает значение типа "ServerFarmWithRichSku" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7d232-136">Parameter 'AppServicePlan' accepts value of type 'ServerFarmWithRichSku' from the pipeline</span></span>

## <span data-ttu-id="7d232-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d232-137">OUTPUTS</span></span>

### <span data-ttu-id="7d232-138">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7d232-138">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

## <span data-ttu-id="7d232-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d232-139">NOTES</span></span>

## <span data-ttu-id="7d232-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d232-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d232-141">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-141">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="7d232-142">New-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-142">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="7d232-143">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-143">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="7d232-144">Restarting-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-144">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="7d232-145">Start-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-145">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)

[<span data-ttu-id="7d232-146">Остановить-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="7d232-146">Stop-AzureRmWebApp</span></span>](./Stop-AzureRmWebApp.md)


