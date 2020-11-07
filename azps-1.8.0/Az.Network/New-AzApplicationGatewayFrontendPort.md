---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 26b6bc0128929efda2baf52979e1b6c2ecdbd714
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730408"
---
# <span data-ttu-id="daa13-101">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-101">New-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="daa13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="daa13-102">SYNOPSIS</span></span>
<span data-ttu-id="daa13-103">Создает интерфейсный порт для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="daa13-103">Creates a front-end port for an application gateway.</span></span>

## <span data-ttu-id="daa13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="daa13-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFrontendPort -Name <String> -Port <Int32> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="daa13-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="daa13-105">DESCRIPTION</span></span>
<span data-ttu-id="daa13-106">Командлет **New-AzApplicationGatewayFrontendPort** создает интерфейсный порт для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="daa13-106">The **New-AzApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="daa13-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="daa13-107">EXAMPLES</span></span>

### <span data-ttu-id="daa13-108">Example1: создание внешнего порта</span><span class="sxs-lookup"><span data-stu-id="daa13-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="daa13-109">Эта команда создает интерфейсный порт с именем FrontEndPort01 на порту 80 и сохраняет результат в переменной с именем $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="daa13-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="daa13-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="daa13-110">PARAMETERS</span></span>

### <span data-ttu-id="daa13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daa13-111">-DefaultProfile</span></span>
<span data-ttu-id="daa13-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="daa13-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daa13-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="daa13-113">-Name</span></span>
<span data-ttu-id="daa13-114">Указывает имя порта переднего плана, созданного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="daa13-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="daa13-115">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="daa13-115">-Port</span></span>
<span data-ttu-id="daa13-116">Задает номер порта переднего порта.</span><span class="sxs-lookup"><span data-stu-id="daa13-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="daa13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daa13-117">CommonParameters</span></span>
<span data-ttu-id="daa13-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="daa13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daa13-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daa13-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daa13-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="daa13-120">INPUTS</span></span>

### <span data-ttu-id="daa13-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="daa13-121">None</span></span>

## <span data-ttu-id="daa13-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="daa13-122">OUTPUTS</span></span>

### <span data-ttu-id="daa13-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="daa13-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="daa13-124">NOTES</span></span>

## <span data-ttu-id="daa13-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="daa13-125">RELATED LINKS</span></span>

[<span data-ttu-id="daa13-126">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-126">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="daa13-127">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-127">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="daa13-128">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-128">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="daa13-129">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="daa13-129">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


