---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: c37c55539f983b490c917e1fe062f14b252ee477
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733451"
---
# <span data-ttu-id="539cc-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="539cc-101">Get-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="539cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="539cc-102">SYNOPSIS</span></span>
<span data-ttu-id="539cc-103">Получает доверенный корневой сертификат с определенным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="539cc-103">Gets the Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="539cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="539cc-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayTrustedRootCertificate [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="539cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="539cc-105">DESCRIPTION</span></span>
<span data-ttu-id="539cc-106">Командлет **Get-AzureRmApplicationGatewayTrustedRootCertificate** получает доверенный корневой сертификат с определенным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="539cc-106">The **Get-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet gets Trusted Root Certificate with a specific name from the Application Gateway.</span></span>

## <span data-ttu-id="539cc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="539cc-107">EXAMPLES</span></span>

### <span data-ttu-id="539cc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="539cc-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzureRmApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $trustedRootCert = Get-AzureRmApplicationGatewayTrustedRootCertificate -ApplicationGateway $gw -Name $certName --CertificateFile ".\rootCA.cer"
```

<span data-ttu-id="539cc-109">Первая команда получает шлюз приложения и сохраняет его в $gw переменной.</span><span class="sxs-lookup"><span data-stu-id="539cc-109">The first command gets the Application Gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="539cc-110">Вторая команда получает доверенный корневой сертификат с указанным именем из шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="539cc-110">The second command gets the Trusted Root Certificate with a specified name from the Application Gateway.</span></span>

## <span data-ttu-id="539cc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="539cc-111">PARAMETERS</span></span>

### <span data-ttu-id="539cc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539cc-112">-ApplicationGateway</span></span>
<span data-ttu-id="539cc-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539cc-113">The applicationGateway</span></span>

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

### <span data-ttu-id="539cc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="539cc-114">-DefaultProfile</span></span>
<span data-ttu-id="539cc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="539cc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cc-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="539cc-116">-Name</span></span>
<span data-ttu-id="539cc-117">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="539cc-117">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="539cc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="539cc-118">CommonParameters</span></span>
<span data-ttu-id="539cc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="539cc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="539cc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="539cc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="539cc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="539cc-121">INPUTS</span></span>

### <span data-ttu-id="539cc-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="539cc-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="539cc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="539cc-123">OUTPUTS</span></span>

### <span data-ttu-id="539cc-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="539cc-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="539cc-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="539cc-125">NOTES</span></span>

## <span data-ttu-id="539cc-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="539cc-126">RELATED LINKS</span></span>
