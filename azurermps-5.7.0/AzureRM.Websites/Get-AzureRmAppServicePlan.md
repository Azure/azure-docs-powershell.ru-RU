---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: a46d104a6cd5917d6550d6b78d62a6d50581039e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733530"
---
# <span data-ttu-id="620c4-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="620c4-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="620c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="620c4-102">SYNOPSIS</span></span>
<span data-ttu-id="620c4-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="620c4-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="620c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="620c4-104">SYNTAX</span></span>

### <span data-ttu-id="620c4-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="620c4-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="620c4-106">S2</span><span class="sxs-lookup"><span data-stu-id="620c4-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="620c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="620c4-107">DESCRIPTION</span></span>
<span data-ttu-id="620c4-108">Командлет **Get-AzureRmAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="620c4-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="620c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="620c4-109">EXAMPLES</span></span>

### <span data-ttu-id="620c4-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="620c4-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="620c4-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="620c4-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="620c4-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="620c4-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="620c4-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="620c4-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="620c4-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="620c4-114">PARAMETERS</span></span>

### <span data-ttu-id="620c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620c4-115">-DefaultProfile</span></span>
<span data-ttu-id="620c4-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="620c4-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="620c4-117">-Location</span><span class="sxs-lookup"><span data-stu-id="620c4-117">-Location</span></span>
<span data-ttu-id="620c4-118">Поиска</span><span class="sxs-lookup"><span data-stu-id="620c4-118">Location</span></span> 

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

### <span data-ttu-id="620c4-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="620c4-119">-Name</span></span>
<span data-ttu-id="620c4-120">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="620c4-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="620c4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="620c4-121">-ResourceGroupName</span></span>
<span data-ttu-id="620c4-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="620c4-122">Resource Group Name</span></span>

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

### <span data-ttu-id="620c4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620c4-123">CommonParameters</span></span>
<span data-ttu-id="620c4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="620c4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620c4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620c4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620c4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="620c4-126">INPUTS</span></span>

### <span data-ttu-id="620c4-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="620c4-127">None</span></span>
<span data-ttu-id="620c4-128">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="620c4-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="620c4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="620c4-129">OUTPUTS</span></span>

### <span data-ttu-id="620c4-130">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="620c4-130">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="620c4-131">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="620c4-131">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="620c4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="620c4-132">NOTES</span></span>

## <span data-ttu-id="620c4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="620c4-133">RELATED LINKS</span></span>

[<span data-ttu-id="620c4-134">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="620c4-134">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="620c4-135">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="620c4-135">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="620c4-136">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="620c4-136">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


