---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoverypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: f09ca4bb6c033b954542d6c734b27bf5f2236d87
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557155"
---
# <span data-ttu-id="15d03-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15d03-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="15d03-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15d03-102">SYNOPSIS</span></span>
<span data-ttu-id="15d03-103">Удаление политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="15d03-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15d03-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15d03-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15d03-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15d03-105">DESCRIPTION</span></span>
<span data-ttu-id="15d03-106">Командлет **Remove-AzureRMSiteRecoveryPolicy** удаляет политику репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="15d03-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="15d03-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15d03-107">EXAMPLES</span></span>

## <span data-ttu-id="15d03-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15d03-108">PARAMETERS</span></span>

### <span data-ttu-id="15d03-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d03-109">-DefaultProfile</span></span>
<span data-ttu-id="15d03-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15d03-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15d03-111">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="15d03-111">-Policy</span></span>
<span data-ttu-id="15d03-112">Указывает объект политики восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="15d03-112">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15d03-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d03-113">CommonParameters</span></span>
<span data-ttu-id="15d03-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15d03-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d03-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15d03-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d03-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15d03-116">INPUTS</span></span>

### <span data-ttu-id="15d03-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="15d03-117">ASRPolicy</span></span>
<span data-ttu-id="15d03-118">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="15d03-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="15d03-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15d03-119">OUTPUTS</span></span>

## <span data-ttu-id="15d03-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="15d03-120">NOTES</span></span>

## <span data-ttu-id="15d03-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15d03-121">RELATED LINKS</span></span>

[<span data-ttu-id="15d03-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15d03-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="15d03-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="15d03-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
