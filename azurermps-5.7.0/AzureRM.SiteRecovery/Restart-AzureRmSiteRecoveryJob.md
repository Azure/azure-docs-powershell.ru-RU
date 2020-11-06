---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557132"
---
# <span data-ttu-id="5817a-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5817a-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="5817a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5817a-102">SYNOPSIS</span></span>
<span data-ttu-id="5817a-103">Перезапускает задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5817a-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5817a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5817a-104">SYNTAX</span></span>

### <span data-ttu-id="5817a-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5817a-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5817a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5817a-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5817a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5817a-107">DESCRIPTION</span></span>
<span data-ttu-id="5817a-108">Командлет **restart-AzureRmSiteRecoveryJob** перезапустит задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5817a-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="5817a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5817a-109">EXAMPLES</span></span>

## <span data-ttu-id="5817a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5817a-110">PARAMETERS</span></span>

### <span data-ttu-id="5817a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5817a-111">-DefaultProfile</span></span>
<span data-ttu-id="5817a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5817a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5817a-113">-Job</span><span class="sxs-lookup"><span data-stu-id="5817a-113">-Job</span></span>
<span data-ttu-id="5817a-114">Указывает объект задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="5817a-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5817a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5817a-115">-Name</span></span>
<span data-ttu-id="5817a-116">Указывает уникальное имя задания.</span><span class="sxs-lookup"><span data-stu-id="5817a-116">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5817a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5817a-117">CommonParameters</span></span>
<span data-ttu-id="5817a-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5817a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5817a-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5817a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5817a-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5817a-120">INPUTS</span></span>

### <span data-ttu-id="5817a-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="5817a-121">ASRJob</span></span>
<span data-ttu-id="5817a-122">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5817a-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="5817a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5817a-123">OUTPUTS</span></span>

### <span data-ttu-id="5817a-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5817a-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5817a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="5817a-125">NOTES</span></span>

## <span data-ttu-id="5817a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5817a-126">RELATED LINKS</span></span>

[<span data-ttu-id="5817a-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5817a-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5817a-128">Возобновить — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5817a-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="5817a-129">Остановить-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="5817a-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
