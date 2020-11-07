---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732683"
---
# <span data-ttu-id="3da91-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3da91-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="3da91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3da91-102">SYNOPSIS</span></span>
<span data-ttu-id="3da91-103">Удаление политики репликации восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="3da91-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3da91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3da91-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3da91-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3da91-105">DESCRIPTION</span></span>
<span data-ttu-id="3da91-106">Командлет **Remove-AzureRMSiteRecoveryPolicy** удаляет политику репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="3da91-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="3da91-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3da91-107">EXAMPLES</span></span>

## <span data-ttu-id="3da91-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3da91-108">PARAMETERS</span></span>

### <span data-ttu-id="3da91-109">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="3da91-109">-Policy</span></span>
<span data-ttu-id="3da91-110">Указывает объект политики восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="3da91-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3da91-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3da91-111">-DefaultProfile</span></span>
<span data-ttu-id="3da91-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3da91-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3da91-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3da91-113">CommonParameters</span></span>
<span data-ttu-id="3da91-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3da91-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3da91-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3da91-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3da91-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3da91-116">INPUTS</span></span>

### <span data-ttu-id="3da91-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="3da91-117">ASRPolicy</span></span>
<span data-ttu-id="3da91-118">Параметр "Policy" принимает значение типа "ASRPolicy" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3da91-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="3da91-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3da91-119">OUTPUTS</span></span>

## <span data-ttu-id="3da91-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="3da91-120">NOTES</span></span>

## <span data-ttu-id="3da91-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3da91-121">RELATED LINKS</span></span>

[<span data-ttu-id="3da91-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3da91-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="3da91-123">New-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="3da91-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
