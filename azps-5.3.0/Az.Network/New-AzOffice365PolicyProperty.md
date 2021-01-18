---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9fae8c6d543bddc3ad4110b95a1c1b4a1f146879
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505521"
---
# <span data-ttu-id="69f22-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="69f22-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="69f22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69f22-102">SYNOPSIS</span></span>
<span data-ttu-id="69f22-103">Определите новую политику разбора трафика Office 365, которая будет использоваться с сайтом виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="69f22-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="69f22-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="69f22-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69f22-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f22-105">DESCRIPTION</span></span>
<span data-ttu-id="69f22-106">Команда New-AzOffice365PolicyProperties определяет политику разбора в Office 365, которая будет использоваться с сайтом виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="69f22-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="69f22-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="69f22-107">EXAMPLES</span></span>

### <span data-ttu-id="69f22-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="69f22-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="69f22-109">Создайте объект политики разбора трафика Office 365, который будет использоваться с командами сайта виртуальных устройств.</span><span class="sxs-lookup"><span data-stu-id="69f22-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="69f22-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69f22-110">PARAMETERS</span></span>

### <span data-ttu-id="69f22-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="69f22-111">-Allow</span></span>
<span data-ttu-id="69f22-112">Разорвать трафик категории "Разрешить".</span><span class="sxs-lookup"><span data-stu-id="69f22-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="69f22-113">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="69f22-113">-Default</span></span>
<span data-ttu-id="69f22-114">Разорвать трафик категории по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="69f22-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="69f22-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f22-115">-DefaultProfile</span></span>
<span data-ttu-id="69f22-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69f22-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69f22-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="69f22-117">-Optimize</span></span>
<span data-ttu-id="69f22-118">Разорвать трафик оптимизации категории.</span><span class="sxs-lookup"><span data-stu-id="69f22-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="69f22-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f22-119">CommonParameters</span></span>
<span data-ttu-id="69f22-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69f22-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f22-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="69f22-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f22-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="69f22-122">INPUTS</span></span>

### <span data-ttu-id="69f22-123">Нет</span><span class="sxs-lookup"><span data-stu-id="69f22-123">None</span></span>

## <span data-ttu-id="69f22-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="69f22-124">OUTPUTS</span></span>

### <span data-ttu-id="69f22-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="69f22-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="69f22-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="69f22-126">NOTES</span></span>

## <span data-ttu-id="69f22-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69f22-127">RELATED LINKS</span></span>
