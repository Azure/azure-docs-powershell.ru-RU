---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: dc5a0fb99ca3ce41447cc95ebb42490b88379f83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425380"
---
# <span data-ttu-id="f7d93-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f7d93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7d93-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d93-103">Создается стойкий порт для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="f7d93-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="f7d93-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f7d93-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7d93-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7d93-105">DESCRIPTION</span></span>
<span data-ttu-id="f7d93-106">Для шлюза приложения Azure создается клиентский порт **New-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="f7d93-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="f7d93-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f7d93-107">EXAMPLES</span></span>

### <span data-ttu-id="f7d93-108">Пример 1. Пример 1. Создание переднего порта</span><span class="sxs-lookup"><span data-stu-id="f7d93-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f7d93-109">Эта команда создает стойкий порт FrontEndPort01 в порте 80 и сохраняет результат в переменной с $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f7d93-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="f7d93-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7d93-110">PARAMETERS</span></span>

### <span data-ttu-id="f7d93-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d93-111">-DefaultProfile</span></span>
<span data-ttu-id="f7d93-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d93-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7d93-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f7d93-113">-Name</span></span>
<span data-ttu-id="f7d93-114">Указывает имя переднего порта, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d93-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f7d93-115">-Port</span><span class="sxs-lookup"><span data-stu-id="f7d93-115">-Port</span></span>
<span data-ttu-id="f7d93-116">Определяет номер порта переднего.</span><span class="sxs-lookup"><span data-stu-id="f7d93-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d93-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d93-117">CommonParameters</span></span>
<span data-ttu-id="f7d93-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d93-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d93-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d93-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d93-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d93-120">INPUTS</span></span>

### <span data-ttu-id="f7d93-121">Нет</span><span class="sxs-lookup"><span data-stu-id="f7d93-121">None</span></span>

## <span data-ttu-id="f7d93-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f7d93-122">OUTPUTS</span></span>

### <span data-ttu-id="f7d93-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f7d93-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f7d93-124">NOTES</span></span>

## <span data-ttu-id="f7d93-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7d93-125">RELATED LINKS</span></span>

[<span data-ttu-id="f7d93-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7d93-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7d93-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f7d93-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f7d93-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


