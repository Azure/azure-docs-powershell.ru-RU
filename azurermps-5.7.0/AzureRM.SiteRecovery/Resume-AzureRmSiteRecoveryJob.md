---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563296"
---
# <span data-ttu-id="8ba7b-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="8ba7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ba7b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba7b-103">Возобновляет приостановленное задание восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ba7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ba7b-104">SYNTAX</span></span>

### <span data-ttu-id="8ba7b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ba7b-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ba7b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8ba7b-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ba7b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ba7b-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba7b-108">Командлет **Resume-AzureRmSiteRecoveryJob** возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="8ba7b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ba7b-109">EXAMPLES</span></span>

## <span data-ttu-id="8ba7b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ba7b-110">PARAMETERS</span></span>

### <span data-ttu-id="8ba7b-111">-Примечания</span><span class="sxs-lookup"><span data-stu-id="8ba7b-111">-Comments</span></span>
<span data-ttu-id="8ba7b-112">Указывает комментарии для журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-112">Specifies the comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ba7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba7b-113">-DefaultProfile</span></span>
<span data-ttu-id="8ba7b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ba7b-115">-Job</span><span class="sxs-lookup"><span data-stu-id="8ba7b-115">-Job</span></span>
<span data-ttu-id="8ba7b-116">Указывает объект задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-116">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="8ba7b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ba7b-117">-Name</span></span>
<span data-ttu-id="8ba7b-118">Указывает уникальное имя задания.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-118">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="8ba7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba7b-119">CommonParameters</span></span>
<span data-ttu-id="8ba7b-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba7b-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ba7b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba7b-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ba7b-122">INPUTS</span></span>

### <span data-ttu-id="8ba7b-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-123">ASRJob</span></span>
<span data-ttu-id="8ba7b-124">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="8ba7b-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="8ba7b-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ba7b-125">OUTPUTS</span></span>

### <span data-ttu-id="8ba7b-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8ba7b-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ba7b-127">NOTES</span></span>

## <span data-ttu-id="8ba7b-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ba7b-128">RELATED LINKS</span></span>

[<span data-ttu-id="8ba7b-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8ba7b-130">Restarting-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8ba7b-131">Остановить-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8ba7b-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
