---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverynetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 481d2d414cde32e9d0b99cedd5b942b7bed9b248
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567885"
---
# <span data-ttu-id="0a672-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0a672-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="0a672-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a672-102">SYNOPSIS</span></span>
<span data-ttu-id="0a672-103">Удаляет Сетевое сопоставление из текущего хранилища сайтов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a672-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a672-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a672-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a672-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a672-105">DESCRIPTION</span></span>
<span data-ttu-id="0a672-106">Командлет **Remove-AzureRMSiteRecoveryNetworkMapping** удаляет Сетевое сопоставление из текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0a672-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0a672-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a672-107">EXAMPLES</span></span>

## <span data-ttu-id="0a672-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a672-108">PARAMETERS</span></span>

### <span data-ttu-id="0a672-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a672-109">-DefaultProfile</span></span>
<span data-ttu-id="0a672-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a672-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a672-111">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0a672-111">-NetworkMapping</span></span>
<span data-ttu-id="0a672-112">Указывает объект сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="0a672-112">Specifies the network mapping object.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a672-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a672-113">CommonParameters</span></span>
<span data-ttu-id="0a672-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a672-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a672-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a672-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a672-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a672-116">INPUTS</span></span>

### <span data-ttu-id="0a672-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0a672-117">ASRNetworkMapping</span></span>
<span data-ttu-id="0a672-118">Параметр "NetworkMapping" принимает значение типа "ASRNetworkMapping" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0a672-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="0a672-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a672-119">OUTPUTS</span></span>

### <span data-ttu-id="0a672-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a672-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a672-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a672-121">NOTES</span></span>

## <span data-ttu-id="0a672-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a672-122">RELATED LINKS</span></span>

[<span data-ttu-id="0a672-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0a672-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="0a672-124">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="0a672-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
