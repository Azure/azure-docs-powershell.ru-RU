---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 38a9d9d36d4abdf85149fe9d7da5387468985daf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506838"
---
# <span data-ttu-id="2523d-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2523d-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="2523d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2523d-102">SYNOPSIS</span></span>
<span data-ttu-id="2523d-103">Обновляет шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="2523d-103">Updates an application gateway.</span></span>

## <span data-ttu-id="2523d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2523d-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2523d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2523d-105">DESCRIPTION</span></span>
<span data-ttu-id="2523d-106">Для шлюза приложения Azure обновляется **cmdlet Set-AzApplicationGateway.**</span><span class="sxs-lookup"><span data-stu-id="2523d-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="2523d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2523d-107">EXAMPLES</span></span>

### <span data-ttu-id="2523d-108">Пример 1. Обновление шлюза приложения</span><span class="sxs-lookup"><span data-stu-id="2523d-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name Test -ResourceGroupName Appgwtest
PS C:\>$AppGw.Tag = @{"key"="value"}
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="2523d-109">Эти команды обновляют шлюз приложения с помощью параметров в переменной $AppGw и сохраняет обновленный шлюз в $UpdatedAppGw переменной.</span><span class="sxs-lookup"><span data-stu-id="2523d-109">These commands update the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="2523d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2523d-110">PARAMETERS</span></span>

### <span data-ttu-id="2523d-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2523d-111">-ApplicationGateway</span></span>
<span data-ttu-id="2523d-112">Определяет объект шлюза приложения, представляющий состояние, в котором должен быть установлен шлюз приложения.</span><span class="sxs-lookup"><span data-stu-id="2523d-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2523d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2523d-113">-AsJob</span></span>
<span data-ttu-id="2523d-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2523d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2523d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2523d-115">-DefaultProfile</span></span>
<span data-ttu-id="2523d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2523d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2523d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2523d-117">CommonParameters</span></span>
<span data-ttu-id="2523d-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2523d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2523d-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2523d-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2523d-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2523d-120">INPUTS</span></span>

### <span data-ttu-id="2523d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2523d-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2523d-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2523d-122">OUTPUTS</span></span>

### <span data-ttu-id="2523d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2523d-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2523d-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2523d-124">NOTES</span></span>

## <span data-ttu-id="2523d-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2523d-125">RELATED LINKS</span></span>

[<span data-ttu-id="2523d-126">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2523d-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)

