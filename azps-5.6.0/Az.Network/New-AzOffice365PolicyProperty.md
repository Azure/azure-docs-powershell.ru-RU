---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azoffice365policyproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzOffice365PolicyProperty.md
ms.openlocfilehash: 9e48bfd243133052f526f2b9adcbef2072cdd2cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958355"
---
# <span data-ttu-id="0b560-101">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="0b560-101">New-AzOffice365PolicyProperty</span></span>

## <span data-ttu-id="0b560-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b560-102">SYNOPSIS</span></span>
<span data-ttu-id="0b560-103">Определите новую политику разбора трафика Office 365, которая будет использоваться с сайтом виртуальных устройств.</span><span class="sxs-lookup"><span data-stu-id="0b560-103">Define a new Office 365 traffic breakout policy to be used with a Virtual Appliance site.</span></span>

## <span data-ttu-id="0b560-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b560-104">SYNTAX</span></span>

```
New-AzOffice365PolicyProperty [-Allow] [-Optimize] [-Default] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0b560-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b560-105">DESCRIPTION</span></span>
<span data-ttu-id="0b560-106">Команда New-AzOffice365PolicyProperties определяет политику разборки Office 365, которая будет использоваться с сайтом виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="0b560-106">The New-AzOffice365PolicyProperties command defines an Office 365 breakout policy that is to be used with a Virtual Appliance site.</span></span> 

## <span data-ttu-id="0b560-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b560-107">EXAMPLES</span></span>

### <span data-ttu-id="0b560-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b560-108">Example 1</span></span>
```powershell
PS C:\> $o365Policy = New-AzOffice365PolicyProperty -Allow -Optimize 
```

<span data-ttu-id="0b560-109">Создайте объект политики разбора трафика Office 365, который будет использоваться с командами сайта виртуальных устройств.</span><span class="sxs-lookup"><span data-stu-id="0b560-109">Create Office 365 traffic breakout policy object to be used with Virtual Appliance site commands.</span></span>

## <span data-ttu-id="0b560-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b560-110">PARAMETERS</span></span>

### <span data-ttu-id="0b560-111">-Allow</span><span class="sxs-lookup"><span data-stu-id="0b560-111">-Allow</span></span>
<span data-ttu-id="0b560-112">Разорвать трафик категории "Разрешить".</span><span class="sxs-lookup"><span data-stu-id="0b560-112">Breakout the allow category traffic.</span></span>

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

### <span data-ttu-id="0b560-113">-По умолчанию</span><span class="sxs-lookup"><span data-stu-id="0b560-113">-Default</span></span>
<span data-ttu-id="0b560-114">Разорвать трафик категории по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0b560-114">Breakout the default category traffic.</span></span>

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

### <span data-ttu-id="0b560-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b560-115">-DefaultProfile</span></span>
<span data-ttu-id="0b560-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b560-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b560-117">-Optimize</span><span class="sxs-lookup"><span data-stu-id="0b560-117">-Optimize</span></span>
<span data-ttu-id="0b560-118">Разорвать трафик оптимизации категории.</span><span class="sxs-lookup"><span data-stu-id="0b560-118">Breakout the optimize category traffic.</span></span>

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

### <span data-ttu-id="0b560-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b560-119">CommonParameters</span></span>
<span data-ttu-id="0b560-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b560-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b560-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b560-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b560-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b560-122">INPUTS</span></span>

### <span data-ttu-id="0b560-123">Нет</span><span class="sxs-lookup"><span data-stu-id="0b560-123">None</span></span>

## <span data-ttu-id="0b560-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b560-124">OUTPUTS</span></span>

### <span data-ttu-id="0b560-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span><span class="sxs-lookup"><span data-stu-id="0b560-125">Microsoft.Azure.Commands.Network.Models.PSOffice365PolicyProperties</span></span>

## <span data-ttu-id="0b560-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b560-126">NOTES</span></span>

## <span data-ttu-id="0b560-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b560-127">RELATED LINKS</span></span>
