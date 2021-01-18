---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505777"
---
# <span data-ttu-id="9763e-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9763e-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="9763e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9763e-102">SYNOPSIS</span></span>
<span data-ttu-id="9763e-103">Получите правило маршрутинга для заданного имени слота.</span><span class="sxs-lookup"><span data-stu-id="9763e-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="9763e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9763e-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9763e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9763e-105">DESCRIPTION</span></span>
<span data-ttu-id="9763e-106">Чтобы **получить конфигурацию** правила маршрутирования из слота Azure Web App, можно получить конфигурацию правила маршрутизирования из слота Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="9763e-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="9763e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9763e-107">EXAMPLES</span></span>

### <span data-ttu-id="9763e-108">Пример 1. Получает определенное правило маршрутинга из слота веб-приложения</span><span class="sxs-lookup"><span data-stu-id="9763e-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="9763e-109">Эта команда получает правило маршрутинга для заданного слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="9763e-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="9763e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9763e-110">PARAMETERS</span></span>

### <span data-ttu-id="9763e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9763e-111">-DefaultProfile</span></span>
<span data-ttu-id="9763e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9763e-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9763e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9763e-113">-ResourceGroupName</span></span>
<span data-ttu-id="9763e-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9763e-114">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9763e-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="9763e-115">-RuleName</span></span>
<span data-ttu-id="9763e-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="9763e-116">Rule Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9763e-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="9763e-117">-WebAppName</span></span>
<span data-ttu-id="9763e-118">Имя веб-приложения</span><span class="sxs-lookup"><span data-stu-id="9763e-118">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9763e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9763e-119">CommonParameters</span></span>
<span data-ttu-id="9763e-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9763e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9763e-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9763e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9763e-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9763e-122">INPUTS</span></span>

### <span data-ttu-id="9763e-123">Нет</span><span class="sxs-lookup"><span data-stu-id="9763e-123">None</span></span>

## <span data-ttu-id="9763e-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9763e-124">OUTPUTS</span></span>

### <span data-ttu-id="9763e-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span><span class="sxs-lookup"><span data-stu-id="9763e-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="9763e-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9763e-126">NOTES</span></span>

## <span data-ttu-id="9763e-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9763e-127">RELATED LINKS</span></span>

[<span data-ttu-id="9763e-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9763e-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="9763e-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9763e-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="9763e-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="9763e-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)
