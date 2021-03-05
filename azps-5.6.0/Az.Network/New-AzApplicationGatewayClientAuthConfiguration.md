---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewayclientauthconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayClientAuthConfiguration.md
ms.openlocfilehash: 002fdabfb01a0b12d36c69b0a8a75ddf91880012
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965656"
---
# <span data-ttu-id="5d292-101">New-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-101">New-AzApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="5d292-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d292-102">SYNOPSIS</span></span>
<span data-ttu-id="5d292-103">Создает новую конфигурацию проверки подлинности клиента для профиля SSL.</span><span class="sxs-lookup"><span data-stu-id="5d292-103">Creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="5d292-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d292-104">SYNTAX</span></span>

```
New-AzApplicationGatewayClientAuthConfiguration [-VerifyClientCertIssuerDN]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d292-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d292-105">DESCRIPTION</span></span>
<span data-ttu-id="5d292-106">Для профиля SSL создается новая конфигурация проверки подлинности клиента: **New-AzApplicationGatewayClientAuthConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="5d292-106">The **New-AzApplicationGatewayClientAuthConfiguration** cmdlet creates a new client authentication configuration for SSL profile.</span></span>

## <span data-ttu-id="5d292-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d292-107">EXAMPLES</span></span>

### <span data-ttu-id="5d292-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5d292-108">Example 1</span></span>
```powershell
PS C:\> $clientAuthConfig = New-AzApplicationGatewayClientAuthConfiguration -VerifyClientCertIssuerDN
```

<span data-ttu-id="5d292-109">Команда создает новую конфигурацию клиента и сохраняет ее в $clientAuthConfig переменной, которая будет использоваться в профиле SSL.</span><span class="sxs-lookup"><span data-stu-id="5d292-109">The command create a new client auth configuration and stores it in $clientAuthConfig variable to be used in a SSL profile.</span></span> 

## <span data-ttu-id="5d292-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d292-110">PARAMETERS</span></span>

### <span data-ttu-id="5d292-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d292-111">-DefaultProfile</span></span>
<span data-ttu-id="5d292-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d292-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d292-113">-VerifyClientCertIssuerDN</span><span class="sxs-lookup"><span data-stu-id="5d292-113">-VerifyClientCertIssuerDN</span></span>
<span data-ttu-id="5d292-114">Проверьте имя выпуска сертификата клиента.</span><span class="sxs-lookup"><span data-stu-id="5d292-114">Verify client certificate issuer name.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d292-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d292-115">CommonParameters</span></span>
<span data-ttu-id="5d292-116">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d292-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d292-117">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d292-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d292-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d292-118">INPUTS</span></span>

### <span data-ttu-id="5d292-119">Нет</span><span class="sxs-lookup"><span data-stu-id="5d292-119">None</span></span>

## <span data-ttu-id="5d292-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d292-120">OUTPUTS</span></span>

### <span data-ttu-id="5d292-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayClientAuthConfiguration</span></span>

## <span data-ttu-id="5d292-122">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d292-122">NOTES</span></span>

## <span data-ttu-id="5d292-123">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d292-123">RELATED LINKS</span></span>

[<span data-ttu-id="5d292-124">Add-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-124">Add-AzApplicationGatewayClientAuthConfiguration</span></span>](./Add-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="5d292-125">Get-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-125">Get-AzApplicationGatewayClientAuthConfiguration</span></span>](./Get-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="5d292-126">Remove-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-126">Remove-AzApplicationGatewayClientAuthConfiguration</span></span>](./Remove-AzApplicationGatewayClientAuthConfiguration.md)

[<span data-ttu-id="5d292-127">Set-AzApplicationGatewayClientAuthConfiguration</span><span class="sxs-lookup"><span data-stu-id="5d292-127">Set-AzApplicationGatewayClientAuthConfiguration</span></span>](./Set-AzApplicationGatewayClientAuthConfiguration.md)