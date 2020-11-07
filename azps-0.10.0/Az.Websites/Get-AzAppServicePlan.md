---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/get-Azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: 48d37bf19ec6613ce1f42ee8cf7609bd6383e12f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910632"
---
# <span data-ttu-id="8e4e4-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e4e4-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="8e4e4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8e4e4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4e4-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8e4e4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8e4e4-104">SYNTAX</span></span>

### <span data-ttu-id="8e4e4-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="8e4e4-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e4e4-106">S2</span><span class="sxs-lookup"><span data-stu-id="8e4e4-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e4e4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e4e4-107">DESCRIPTION</span></span>
<span data-ttu-id="8e4e4-108">Командлет **Get-AzAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="8e4e4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8e4e4-109">EXAMPLES</span></span>

### <span data-ttu-id="8e4e4-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8e4e4-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="8e4e4-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="8e4e4-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="8e4e4-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="8e4e4-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="8e4e4-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="8e4e4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8e4e4-114">PARAMETERS</span></span>

### <span data-ttu-id="8e4e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4e4-115">-DefaultProfile</span></span>
<span data-ttu-id="8e4e4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e4e4-117">-Location</span><span class="sxs-lookup"><span data-stu-id="8e4e4-117">-Location</span></span>
<span data-ttu-id="8e4e4-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="8e4e4-118">Location</span></span> 

```yaml
Type: String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4e4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8e4e4-119">-Name</span></span>
<span data-ttu-id="8e4e4-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="8e4e4-120">App Service Plan Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4e4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e4e4-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e4e4-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8e4e4-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e4e4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4e4-123">CommonParameters</span></span>
<span data-ttu-id="8e4e4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4e4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e4e4-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4e4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8e4e4-126">INPUTS</span></span>

### <span data-ttu-id="8e4e4-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="8e4e4-127">None</span></span>
<span data-ttu-id="8e4e4-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8e4e4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8e4e4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e4e4-129">OUTPUTS</span></span>

### <span data-ttu-id="8e4e4-130">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="8e4e4-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="8e4e4-131">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="8e4e4-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="8e4e4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="8e4e4-132">NOTES</span></span>

## <span data-ttu-id="8e4e4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e4e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="8e4e4-134">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e4e4-134">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="8e4e4-135">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e4e4-135">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="8e4e4-136">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="8e4e4-136">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


