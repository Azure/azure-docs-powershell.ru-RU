---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppTrafficRouting.md
ms.openlocfilehash: fb8d23ad24f8e9ab0b6e951d39ba7445d336176f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243432"
---
# <span data-ttu-id="f2bce-101">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f2bce-101">Get-AzWebAppTrafficRouting</span></span>

## <span data-ttu-id="f2bce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2bce-102">SYNOPSIS</span></span>
<span data-ttu-id="f2bce-103">Получение правила маршрутизации для заданных названий гнезд.</span><span class="sxs-lookup"><span data-stu-id="f2bce-103">Get a routing Rule for the given Slot name.</span></span>

## <span data-ttu-id="f2bce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2bce-104">SYNTAX</span></span>

```
Get-AzWebAppTrafficRouting -ResourceGroupName <String> -WebAppName <String> -RuleName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2bce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2bce-105">DESCRIPTION</span></span>
<span data-ttu-id="f2bce-106">Командлет **Get-AzWebAppTrafficRouting** получает конфигурацию правила маршрутизации из слота веб-приложения Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bce-106">The **Get-AzWebAppTrafficRouting** cmdlet Gets a routing rule configuration from an Azure Web App Slot.</span></span>

## <span data-ttu-id="f2bce-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2bce-107">EXAMPLES</span></span>

### <span data-ttu-id="f2bce-108">Например 1 получает конкретное правило маршрутизации из webapp Slot.</span><span class="sxs-lookup"><span data-stu-id="f2bce-108">Example 1 Gets the specific routing rule from webapp slot</span></span>
```powershell
PS C:\> Get-AzWebAppTrafficRouting -ResourceGroupName "Default-Web-WestUS" -WebAppName "ContosoSite"  -RuleName 'Stg'
```

<span data-ttu-id="f2bce-109">Эта команда возвращает правило маршрутизации для заданной webapp ячейки.</span><span class="sxs-lookup"><span data-stu-id="f2bce-109">This command gets a routing rule for a given webapp slot.</span></span>

## <span data-ttu-id="f2bce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2bce-110">PARAMETERS</span></span>

### <span data-ttu-id="f2bce-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2bce-111">-DefaultProfile</span></span>
<span data-ttu-id="f2bce-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2bce-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2bce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2bce-113">-ResourceGroupName</span></span>
<span data-ttu-id="f2bce-114">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f2bce-114">Resource Group Name</span></span>

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

### <span data-ttu-id="f2bce-115">-RuleName</span><span class="sxs-lookup"><span data-stu-id="f2bce-115">-RuleName</span></span>
<span data-ttu-id="f2bce-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="f2bce-116">Rule Name</span></span>
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

### <span data-ttu-id="f2bce-117">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="f2bce-117">-WebAppName</span></span>
<span data-ttu-id="f2bce-118">Имя WebApp</span><span class="sxs-lookup"><span data-stu-id="f2bce-118">WebApp Name</span></span>

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

### <span data-ttu-id="f2bce-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2bce-119">CommonParameters</span></span>
<span data-ttu-id="f2bce-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2bce-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2bce-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2bce-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2bce-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2bce-122">INPUTS</span></span>

### <span data-ttu-id="f2bce-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="f2bce-123">None</span></span>

## <span data-ttu-id="f2bce-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2bce-124">OUTPUTS</span></span>

### <span data-ttu-id="f2bce-125">Microsoft. Azure. Management. website. Models. RampUpRule</span><span class="sxs-lookup"><span data-stu-id="f2bce-125">Microsoft.Azure.Management.WebSites.Models.RampUpRule</span></span>

## <span data-ttu-id="f2bce-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2bce-126">NOTES</span></span>

## <span data-ttu-id="f2bce-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2bce-127">RELATED LINKS</span></span>

[<span data-ttu-id="f2bce-128">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f2bce-128">Update-AzWebAppTrafficRouting</span></span>](./Update-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f2bce-129">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f2bce-129">Add-AzWebAppTrafficRouting</span></span>](./Add-AzWebAppTrafficRouting.md)

[<span data-ttu-id="f2bce-130">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="f2bce-130">Remove-AzWebAppTrafficRouting</span></span>](./Remove-AzWebAppTrafficRouting.md)