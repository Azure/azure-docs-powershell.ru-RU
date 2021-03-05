---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: bbe4cf87c3af86cd8a4e72f239d4aca7c3386786
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981363"
---
# <span data-ttu-id="a66ae-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a66ae-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="a66ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a66ae-102">SYNOPSIS</span></span>
<span data-ttu-id="a66ae-103">Получает план службы приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a66ae-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="a66ae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a66ae-104">SYNTAX</span></span>

### <span data-ttu-id="a66ae-105">S1</span><span class="sxs-lookup"><span data-stu-id="a66ae-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a66ae-106">S2</span><span class="sxs-lookup"><span data-stu-id="a66ae-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a66ae-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a66ae-107">DESCRIPTION</span></span>
<span data-ttu-id="a66ae-108">С **помощью cmdlet Get-AzAppServicePlan** можно получить план службы приложения Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a66ae-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="a66ae-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a66ae-109">EXAMPLES</span></span>

### <span data-ttu-id="a66ae-110">Пример 1. Получить план службы приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a66ae-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="a66ae-111">Эта команда получает план службы приложений ContosoASP, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="a66ae-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="a66ae-112">Пример 2. Получить все планы служб приложений в одном месте</span><span class="sxs-lookup"><span data-stu-id="a66ae-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="a66ae-113">Эта команда получает все планы служб приложений, расположенные в регионе "Запад США".</span><span class="sxs-lookup"><span data-stu-id="a66ae-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="a66ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a66ae-114">PARAMETERS</span></span>

### <span data-ttu-id="a66ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66ae-115">-DefaultProfile</span></span>
<span data-ttu-id="a66ae-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a66ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66ae-117">-Location</span><span class="sxs-lookup"><span data-stu-id="a66ae-117">-Location</span></span>
<span data-ttu-id="a66ae-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="a66ae-118">Location</span></span> 

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

### <span data-ttu-id="a66ae-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a66ae-119">-Name</span></span>
<span data-ttu-id="a66ae-120">Название плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="a66ae-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="a66ae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a66ae-121">-ResourceGroupName</span></span>
<span data-ttu-id="a66ae-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="a66ae-122">Resource Group Name</span></span>

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

### <span data-ttu-id="a66ae-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66ae-123">CommonParameters</span></span>
<span data-ttu-id="a66ae-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66ae-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66ae-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66ae-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66ae-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a66ae-126">INPUTS</span></span>

### <span data-ttu-id="a66ae-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a66ae-127">None</span></span>

## <span data-ttu-id="a66ae-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a66ae-128">OUTPUTS</span></span>

### <span data-ttu-id="a66ae-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a66ae-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="a66ae-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a66ae-130">NOTES</span></span>

## <span data-ttu-id="a66ae-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a66ae-131">RELATED LINKS</span></span>

[<span data-ttu-id="a66ae-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a66ae-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="a66ae-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a66ae-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="a66ae-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="a66ae-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


