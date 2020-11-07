---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733310"
---
# <span data-ttu-id="b313e-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b313e-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="b313e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b313e-102">SYNOPSIS</span></span>
<span data-ttu-id="b313e-103">Возобновляет приостановленное задание восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b313e-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b313e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b313e-104">SYNTAX</span></span>

### <span data-ttu-id="b313e-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b313e-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b313e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b313e-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b313e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b313e-107">DESCRIPTION</span></span>
<span data-ttu-id="b313e-108">Командлет **Resume-AzureRmSiteRecoveryJob** возобновляет приостановленное задание восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b313e-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="b313e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b313e-109">EXAMPLES</span></span>

## <span data-ttu-id="b313e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b313e-110">PARAMETERS</span></span>

### <span data-ttu-id="b313e-111">-Примечания</span><span class="sxs-lookup"><span data-stu-id="b313e-111">-Comments</span></span>
<span data-ttu-id="b313e-112">Указывает комментарии для журнала заданий.</span><span class="sxs-lookup"><span data-stu-id="b313e-112">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="b313e-113">-Job</span><span class="sxs-lookup"><span data-stu-id="b313e-113">-Job</span></span>
<span data-ttu-id="b313e-114">Указывает объект задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="b313e-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b313e-115">-Name</span></span>
<span data-ttu-id="b313e-116">Указывает уникальное имя задания.</span><span class="sxs-lookup"><span data-stu-id="b313e-116">Specifies the unique name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b313e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b313e-117">-DefaultProfile</span></span>
<span data-ttu-id="b313e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b313e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b313e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b313e-119">CommonParameters</span></span>
<span data-ttu-id="b313e-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b313e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b313e-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b313e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b313e-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b313e-122">INPUTS</span></span>

### <span data-ttu-id="b313e-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="b313e-123">ASRJob</span></span>
<span data-ttu-id="b313e-124">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b313e-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="b313e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b313e-125">OUTPUTS</span></span>

### <span data-ttu-id="b313e-126">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b313e-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b313e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="b313e-127">NOTES</span></span>

## <span data-ttu-id="b313e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b313e-128">RELATED LINKS</span></span>

[<span data-ttu-id="b313e-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b313e-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="b313e-130">Restarting-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b313e-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="b313e-131">Остановить-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="b313e-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
