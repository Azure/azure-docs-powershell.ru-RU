---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmAppServicePlan.md
ms.openlocfilehash: 9cadc32a34f94a29221984e25141bcc3a844de4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733079"
---
# <span data-ttu-id="7d6ee-101">Get-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d6ee-101">Get-AzureRmAppServicePlan</span></span>

## <span data-ttu-id="7d6ee-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6ee-103">Получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d6ee-103">Gets an Azure App Service plan in the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6ee-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d6ee-104">SYNTAX</span></span>

### <span data-ttu-id="7d6ee-105">Состояний</span><span class="sxs-lookup"><span data-stu-id="7d6ee-105">S1</span></span>
```
Get-AzureRmAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d6ee-106">S2</span><span class="sxs-lookup"><span data-stu-id="7d6ee-106">S2</span></span>
```
Get-AzureRmAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d6ee-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6ee-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6ee-108">Командлет **Get-AzureRmAppServicePlan** получает план служб приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7d6ee-108">The **Get-AzureRmAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="7d6ee-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d6ee-109">EXAMPLES</span></span>

### <span data-ttu-id="7d6ee-110">Пример 1: получение плана служб приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d6ee-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="7d6ee-111">Эта команда получает план служб приложений с именем ContosoASP, который принадлежит группе ресурсов с именем Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="7d6ee-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="7d6ee-112">Пример 2: получение всех планов служб приложений в местоположении</span><span class="sxs-lookup"><span data-stu-id="7d6ee-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzureRmAppServicePlan -Location "West US"
```

<span data-ttu-id="7d6ee-113">Эта команда получает все планы служб приложений, которые находятся в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="7d6ee-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="7d6ee-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d6ee-114">PARAMETERS</span></span>

### <span data-ttu-id="7d6ee-115">-Location</span><span class="sxs-lookup"><span data-stu-id="7d6ee-115">-Location</span></span>
<span data-ttu-id="7d6ee-116">Поиска</span><span class="sxs-lookup"><span data-stu-id="7d6ee-116">Location</span></span> 

```yaml
Type: System.String
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ee-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d6ee-117">-Name</span></span>
<span data-ttu-id="7d6ee-118">Имя плана служб приложений</span><span class="sxs-lookup"><span data-stu-id="7d6ee-118">App Service Plan Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d6ee-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7d6ee-120">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6ee-121">-DefaultProfile</span></span>
<span data-ttu-id="7d6ee-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7d6ee-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d6ee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6ee-123">CommonParameters</span></span>
<span data-ttu-id="7d6ee-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d6ee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6ee-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6ee-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6ee-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d6ee-126">INPUTS</span></span>

## <span data-ttu-id="7d6ee-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6ee-127">OUTPUTS</span></span>

### <span data-ttu-id="7d6ee-128">Microsoft. Azure. Management. website. Models. ServerFarmWithRichSku</span><span class="sxs-lookup"><span data-stu-id="7d6ee-128">Microsoft.Azure.Management.WebSites.Models.ServerFarmWithRichSku</span></span>

### <span data-ttu-id="7d6ee-129">Microsoft. Azure. Management. website. Models. ServerFarmCollection</span><span class="sxs-lookup"><span data-stu-id="7d6ee-129">Microsoft.Azure.Management.WebSites.Models.ServerFarmCollection</span></span>

## <span data-ttu-id="7d6ee-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d6ee-130">NOTES</span></span>

## <span data-ttu-id="7d6ee-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d6ee-131">RELATED LINKS</span></span>

[<span data-ttu-id="7d6ee-132">New-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d6ee-132">New-AzureRmAppServicePlan</span></span>](./New-AzureRmAppServicePlan.md)

[<span data-ttu-id="7d6ee-133">Remove-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d6ee-133">Remove-AzureRmAppServicePlan</span></span>](./Remove-AzureRmAppServicePlan.md)

[<span data-ttu-id="7d6ee-134">Set-AzureRmAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="7d6ee-134">Set-AzureRmAppServicePlan</span></span>](./Set-AzureRmAppServicePlan.md)


