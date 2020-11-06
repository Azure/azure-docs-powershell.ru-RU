---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: b6016857054d2560602c7ea37a508317ff895d37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563288"
---
# <span data-ttu-id="facfc-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="facfc-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="facfc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="facfc-102">SYNOPSIS</span></span>
<span data-ttu-id="facfc-103">Задает контекст хранилища для восстановления сайта для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="facfc-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="facfc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="facfc-104">SYNTAX</span></span>

### <span data-ttu-id="facfc-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="facfc-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="facfc-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="facfc-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="facfc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="facfc-107">DESCRIPTION</span></span>
<span data-ttu-id="facfc-108">Командлет **Set-AzureRmSiteRecoveryVaultSettings** задает контекст хранилища Azure Site Recovery для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="facfc-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="facfc-109">Это не относится к хранилищу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="facfc-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="facfc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="facfc-110">EXAMPLES</span></span>

## <span data-ttu-id="facfc-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="facfc-111">PARAMETERS</span></span>

### <span data-ttu-id="facfc-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="facfc-112">-ARSVault</span></span>
<span data-ttu-id="facfc-113">Указывает объект **ARSVault** .</span><span class="sxs-lookup"><span data-stu-id="facfc-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="facfc-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="facfc-114">-ASRVault</span></span>
<span data-ttu-id="facfc-115">Указывает объект **ASRVault** .</span><span class="sxs-lookup"><span data-stu-id="facfc-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="facfc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="facfc-116">-DefaultProfile</span></span>
<span data-ttu-id="facfc-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="facfc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="facfc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="facfc-118">CommonParameters</span></span>
<span data-ttu-id="facfc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="facfc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="facfc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="facfc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="facfc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="facfc-121">INPUTS</span></span>

### <span data-ttu-id="facfc-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="facfc-122">ARSVault</span></span>
<span data-ttu-id="facfc-123">Параметр "ARSVault" принимает значение типа "ARSVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="facfc-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="facfc-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="facfc-124">ASRVault</span></span>
<span data-ttu-id="facfc-125">Параметр "ASRVault" принимает значение типа "ASRVault" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="facfc-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="facfc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="facfc-126">OUTPUTS</span></span>

### <span data-ttu-id="facfc-127">Microsoft. Azure. Commands. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="facfc-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="facfc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="facfc-128">NOTES</span></span>

## <span data-ttu-id="facfc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="facfc-129">RELATED LINKS</span></span>

[<span data-ttu-id="facfc-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="facfc-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
