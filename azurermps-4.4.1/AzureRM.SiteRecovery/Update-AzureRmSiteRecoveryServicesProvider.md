---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733613"
---
# <span data-ttu-id="2276e-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2276e-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="2276e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2276e-102">SYNOPSIS</span></span>
<span data-ttu-id="2276e-103">Обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2276e-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2276e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2276e-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2276e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2276e-105">DESCRIPTION</span></span>
<span data-ttu-id="2276e-106">Командлет **Update-AzureRmSiteRecoveryServicesProvider** обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2276e-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="2276e-107">Этот командлет можно использовать для активации обновления данных, полученных от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="2276e-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="2276e-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2276e-108">EXAMPLES</span></span>

## <span data-ttu-id="2276e-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2276e-109">PARAMETERS</span></span>

### <span data-ttu-id="2276e-110">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2276e-110">-ServicesProvider</span></span>
<span data-ttu-id="2276e-111">Указывает объект поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2276e-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2276e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2276e-112">-DefaultProfile</span></span>
<span data-ttu-id="2276e-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2276e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2276e-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2276e-114">CommonParameters</span></span>
<span data-ttu-id="2276e-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2276e-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2276e-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2276e-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2276e-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2276e-117">INPUTS</span></span>

### <span data-ttu-id="2276e-118">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2276e-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="2276e-119">Параметр "ServicesProvider" принимает значение типа "ASRRecoveryServicesProvider" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2276e-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="2276e-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2276e-120">OUTPUTS</span></span>

## <span data-ttu-id="2276e-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="2276e-121">NOTES</span></span>

## <span data-ttu-id="2276e-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2276e-122">RELATED LINKS</span></span>

[<span data-ttu-id="2276e-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2276e-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="2276e-124">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="2276e-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
