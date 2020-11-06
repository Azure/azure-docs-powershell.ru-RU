---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569815"
---
# <span data-ttu-id="7934b-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7934b-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7934b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7934b-102">SYNOPSIS</span></span>
<span data-ttu-id="7934b-103">Создает доверенный корневой сертификат для шлюза приложения.</span><span class="sxs-lookup"><span data-stu-id="7934b-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7934b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7934b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7934b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7934b-105">DESCRIPTION</span></span>
<span data-ttu-id="7934b-106">Командлет **New-AzureRmApplicationGatewayTrustedRootCertificate** создает доверенный корневой сертификат для шлюза приложений Azure.</span><span class="sxs-lookup"><span data-stu-id="7934b-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="7934b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7934b-107">EXAMPLES</span></span>

### <span data-ttu-id="7934b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7934b-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="7934b-109">Эта команда создает доверенный корневой сертификат с именем List "trc1" и сохраняет результат в переменной с именем $trc.</span><span class="sxs-lookup"><span data-stu-id="7934b-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="7934b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7934b-110">PARAMETERS</span></span>

### <span data-ttu-id="7934b-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="7934b-111">-CertificateFile</span></span>
<span data-ttu-id="7934b-112">Путь к файлу CER сертификата</span><span class="sxs-lookup"><span data-stu-id="7934b-112">Path of certificate CER file</span></span>

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

### <span data-ttu-id="7934b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7934b-113">-DefaultProfile</span></span>
<span data-ttu-id="7934b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7934b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7934b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7934b-115">-Name</span></span>
<span data-ttu-id="7934b-116">Имя сертификата TrustedRoot</span><span class="sxs-lookup"><span data-stu-id="7934b-116">The name of the TrustedRoot certificate</span></span>

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

### <span data-ttu-id="7934b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7934b-117">-Confirm</span></span>
<span data-ttu-id="7934b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7934b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7934b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7934b-119">-WhatIf</span></span>
<span data-ttu-id="7934b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7934b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7934b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7934b-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7934b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7934b-122">CommonParameters</span></span>
<span data-ttu-id="7934b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7934b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7934b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7934b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7934b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7934b-125">INPUTS</span></span>

### <span data-ttu-id="7934b-126">Ничего</span><span class="sxs-lookup"><span data-stu-id="7934b-126">None</span></span>

## <span data-ttu-id="7934b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7934b-127">OUTPUTS</span></span>

### <span data-ttu-id="7934b-128">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="7934b-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="7934b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="7934b-129">NOTES</span></span>

## <span data-ttu-id="7934b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7934b-130">RELATED LINKS</span></span>
