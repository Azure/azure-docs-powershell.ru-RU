---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566898"
---
# <span data-ttu-id="51f46-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51f46-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="51f46-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51f46-102">SYNOPSIS</span></span>
<span data-ttu-id="51f46-103">Обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="51f46-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f46-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51f46-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="51f46-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51f46-105">DESCRIPTION</span></span>
<span data-ttu-id="51f46-106">Командлет **Update-AzureRmSiteRecoveryServicesProvider** обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="51f46-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="51f46-107">Этот командлет можно использовать для активации обновления данных, полученных от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="51f46-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="51f46-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51f46-108">EXAMPLES</span></span>

## <span data-ttu-id="51f46-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51f46-109">PARAMETERS</span></span>

### <span data-ttu-id="51f46-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f46-110">-DefaultProfile</span></span>
<span data-ttu-id="51f46-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51f46-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f46-112">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51f46-112">-ServicesProvider</span></span>
<span data-ttu-id="51f46-113">Указывает объект поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="51f46-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51f46-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f46-114">CommonParameters</span></span>
<span data-ttu-id="51f46-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51f46-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f46-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f46-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f46-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51f46-117">INPUTS</span></span>

### <span data-ttu-id="51f46-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51f46-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="51f46-119">Параметр "ServicesProvider" принимает значение типа "ASRRecoveryServicesProvider" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="51f46-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="51f46-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51f46-120">OUTPUTS</span></span>

## <span data-ttu-id="51f46-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="51f46-121">NOTES</span></span>

## <span data-ttu-id="51f46-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51f46-122">RELATED LINKS</span></span>

[<span data-ttu-id="51f46-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51f46-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="51f46-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="51f46-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
