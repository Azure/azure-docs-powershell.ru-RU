---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: bcc7335076a0f74c89cede8c6fed66f55d88ec9d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953944"
---
# <span data-ttu-id="9babe-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9babe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9babe-102">SYNOPSIS</span></span>
<span data-ttu-id="9babe-103">Создается стойкий порт для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="9babe-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="9babe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9babe-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9babe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9babe-105">DESCRIPTION</span></span>
<span data-ttu-id="9babe-106">Для шлюза приложения Azure создается клиентский порт **New-AzApplicationGatewayFrontendPort.**</span><span class="sxs-lookup"><span data-stu-id="9babe-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="9babe-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9babe-107">EXAMPLES</span></span>

### <span data-ttu-id="9babe-108">Пример 1. Пример 1. Создание переднего порта</span><span class="sxs-lookup"><span data-stu-id="9babe-108">Example 1: Example1: Create a front-end port</span></span>
```powershell
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="9babe-109">Эта команда создает порт FrontEndPort01 в порте 80 и сохраняет результат в переменной с $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="9babe-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="9babe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9babe-110">PARAMETERS</span></span>

### <span data-ttu-id="9babe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9babe-111">-DefaultProfile</span></span>
<span data-ttu-id="9babe-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9babe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9babe-113">-Name</span><span class="sxs-lookup"><span data-stu-id="9babe-113">-Name</span></span>
<span data-ttu-id="9babe-114">Указывает имя переднего порта, который создает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9babe-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9babe-115">-Port</span><span class="sxs-lookup"><span data-stu-id="9babe-115">-Port</span></span>
<span data-ttu-id="9babe-116">Определяет номер порта переднего.</span><span class="sxs-lookup"><span data-stu-id="9babe-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="9babe-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9babe-117">CommonParameters</span></span>
<span data-ttu-id="9babe-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9babe-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9babe-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9babe-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9babe-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9babe-120">INPUTS</span></span>

### <span data-ttu-id="9babe-121">Нет</span><span class="sxs-lookup"><span data-stu-id="9babe-121">None</span></span>

## <span data-ttu-id="9babe-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9babe-122">OUTPUTS</span></span>

### <span data-ttu-id="9babe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="9babe-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9babe-124">NOTES</span></span>

## <span data-ttu-id="9babe-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9babe-125">RELATED LINKS</span></span>

[<span data-ttu-id="9babe-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9babe-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9babe-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="9babe-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="9babe-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


