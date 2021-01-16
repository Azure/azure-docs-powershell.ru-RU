---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 89ED4231-7616-47D0-BDAA-D849C245DC79
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azappserviceplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzAppServicePlan.md
ms.openlocfilehash: afbee0d6b13c1ce42931a2379cff6aa7ee0127b9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329353"
---
# <span data-ttu-id="6347c-101">Get-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6347c-101">Get-AzAppServicePlan</span></span>

## <span data-ttu-id="6347c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6347c-102">SYNOPSIS</span></span>
<span data-ttu-id="6347c-103">Получает план службы приложений Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6347c-103">Gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6347c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6347c-104">SYNTAX</span></span>

### <span data-ttu-id="6347c-105">S1</span><span class="sxs-lookup"><span data-stu-id="6347c-105">S1</span></span>
```
Get-AzAppServicePlan [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6347c-106">S2</span><span class="sxs-lookup"><span data-stu-id="6347c-106">S2</span></span>
```
Get-AzAppServicePlan [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6347c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6347c-107">DESCRIPTION</span></span>
<span data-ttu-id="6347c-108">С **помощью cmdlet Get-AzAppServicePlan** можно получить план службы приложения Azure в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6347c-108">The **Get-AzAppServicePlan** cmdlet gets an Azure App Service plan in the specified resource group.</span></span>

## <span data-ttu-id="6347c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6347c-109">EXAMPLES</span></span>

### <span data-ttu-id="6347c-110">Пример 1. Получить план службы приложений из группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6347c-110">Example 1: Get an App Service plan from a resource group</span></span>
```
PS C:\>Get-AzAppServicePlan -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="6347c-111">Эта команда получает план службы приложений ContosoASP, который принадлежит к группе ресурсов Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="6347c-111">This command gets the App Service plan named ContosoASP that belongs to the resource group named Default-Web-WestUS.</span></span>

### <span data-ttu-id="6347c-112">Пример 2. Получить все планы служб приложений в одном расположении</span><span class="sxs-lookup"><span data-stu-id="6347c-112">Example 2: Get all App Service plans in a location</span></span>
```
PS C:\>Get-AzAppServicePlan -Location "West US"
```

<span data-ttu-id="6347c-113">Эта команда получает все планы служб приложений, расположенные в регионе "Запад США".</span><span class="sxs-lookup"><span data-stu-id="6347c-113">This command gets all App Service plans located in the "West US" region.</span></span>

## <span data-ttu-id="6347c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6347c-114">PARAMETERS</span></span>

### <span data-ttu-id="6347c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6347c-115">-DefaultProfile</span></span>
<span data-ttu-id="6347c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6347c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6347c-117">-Location</span><span class="sxs-lookup"><span data-stu-id="6347c-117">-Location</span></span>
<span data-ttu-id="6347c-118">Расположение</span><span class="sxs-lookup"><span data-stu-id="6347c-118">Location</span></span> 

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

### <span data-ttu-id="6347c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6347c-119">-Name</span></span>
<span data-ttu-id="6347c-120">Имя плана службы приложений</span><span class="sxs-lookup"><span data-stu-id="6347c-120">App Service Plan Name</span></span>

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

### <span data-ttu-id="6347c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6347c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6347c-122">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="6347c-122">Resource Group Name</span></span>

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

### <span data-ttu-id="6347c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6347c-123">CommonParameters</span></span>
<span data-ttu-id="6347c-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6347c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6347c-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6347c-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6347c-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6347c-126">INPUTS</span></span>

### <span data-ttu-id="6347c-127">Нет</span><span class="sxs-lookup"><span data-stu-id="6347c-127">None</span></span>

## <span data-ttu-id="6347c-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6347c-128">OUTPUTS</span></span>

### <span data-ttu-id="6347c-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6347c-129">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSAppServicePlan</span></span>

## <span data-ttu-id="6347c-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6347c-130">NOTES</span></span>

## <span data-ttu-id="6347c-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6347c-131">RELATED LINKS</span></span>

[<span data-ttu-id="6347c-132">New-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6347c-132">New-AzAppServicePlan</span></span>](./New-AzAppServicePlan.md)

[<span data-ttu-id="6347c-133">Remove-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6347c-133">Remove-AzAppServicePlan</span></span>](./Remove-AzAppServicePlan.md)

[<span data-ttu-id="6347c-134">Set-AzAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="6347c-134">Set-AzAppServicePlan</span></span>](./Set-AzAppServicePlan.md)


