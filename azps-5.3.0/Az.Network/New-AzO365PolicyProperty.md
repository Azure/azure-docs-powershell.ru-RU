---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azo365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzO365PolicyProperty.md
ms.openlocfilehash: 2aeb26447c5684b57d966c403a256fe3d1361a41
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506087"
---
# <span data-ttu-id="4e169-101">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="4e169-101">New-AzO365PolicyProperty</span></span>

## <span data-ttu-id="4e169-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e169-102">SYNOPSIS</span></span>
<span data-ttu-id="4e169-103">Создайте объект политики разорва трафика Office 365.</span><span class="sxs-lookup"><span data-stu-id="4e169-103">Create an office 365 traffic breakout policy object.</span></span>

## <span data-ttu-id="4e169-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e169-104">SYNTAX</span></span>

```
New-AzO365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e169-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e169-105">DESCRIPTION</span></span>
<span data-ttu-id="4e169-106">Создайте политику разорва office 365, которая будет использоваться с New-AzVpnSite и Update-AzVpnSite другими.</span><span class="sxs-lookup"><span data-stu-id="4e169-106">Create an office 365 breakout policy to be used with New-AzVpnSite and Update-AzVpnSite cmdlets.</span></span>
## <span data-ttu-id="4e169-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e169-107">EXAMPLES</span></span>

### <span data-ttu-id="4e169-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4e169-108">Example 1</span></span>
```powershell
PS C:\> $policy = New-AzO365PolicyProperty -Allow -Optimize
```

<span data-ttu-id="4e169-109">Создайте политику разорвать трафик Office 365 с разрешением и оптимизацией категории трафика.</span><span class="sxs-lookup"><span data-stu-id="4e169-109">Create an office 365 traffic breakout policy with breakout allowed for allow and optimize category of traffic.</span></span>

## <span data-ttu-id="4e169-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e169-110">PARAMETERS</span></span>

### <span data-ttu-id="4e169-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="4e169-111">-Allow</span></span>
<span data-ttu-id="4e169-112">Разорвать трафик категории "Разрешить".</span><span class="sxs-lookup"><span data-stu-id="4e169-112">Breakout the allow category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e169-113">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="4e169-113">-Default</span></span>
<span data-ttu-id="4e169-114">Разорвать трафик категории по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4e169-114">Breakout the default category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e169-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e169-115">-DefaultProfile</span></span>
<span data-ttu-id="4e169-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e169-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e169-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="4e169-117">-Optimize</span></span>
<span data-ttu-id="4e169-118">Разорвать трафик оптимизации категории.</span><span class="sxs-lookup"><span data-stu-id="4e169-118">Breakout the optimize category traffic.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e169-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e169-119">CommonParameters</span></span>
<span data-ttu-id="4e169-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e169-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e169-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e169-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e169-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e169-122">INPUTS</span></span>

### <span data-ttu-id="4e169-123">Нет</span><span class="sxs-lookup"><span data-stu-id="4e169-123">None</span></span>

## <span data-ttu-id="4e169-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e169-124">OUTPUTS</span></span>

### <span data-ttu-id="4e169-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="4e169-125">Microsoft.Azure.Commands.Network.Models.PSO365PolicyProperties</span></span>

## <span data-ttu-id="4e169-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e169-126">NOTES</span></span>

## <span data-ttu-id="4e169-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e169-127">RELATED LINKS</span></span>
