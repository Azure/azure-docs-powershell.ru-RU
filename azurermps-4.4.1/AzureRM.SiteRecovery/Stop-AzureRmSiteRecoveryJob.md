---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: CFEA76B4-684C-4C2A-9806-36DC133AEE80
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Stop-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 79ad35a00fcd0aef62e99a217071589e10f973c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562067"
---
# <span data-ttu-id="d89ce-101">Stop-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-101">Stop-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="d89ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d89ce-102">SYNOPSIS</span></span>
<span data-ttu-id="d89ce-103">Остановка задания по восстановлению сайта.</span><span class="sxs-lookup"><span data-stu-id="d89ce-103">Stops a Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d89ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d89ce-104">SYNTAX</span></span>

### <span data-ttu-id="d89ce-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d89ce-105">ByObject (Default)</span></span>
```
Stop-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d89ce-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d89ce-106">ByName</span></span>
```
Stop-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d89ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d89ce-107">DESCRIPTION</span></span>
<span data-ttu-id="d89ce-108">Командлет **Stop-AzureRmSiteRecoveryJob** останавливает задание Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d89ce-108">The **Stop-AzureRmSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="d89ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d89ce-109">EXAMPLES</span></span>

## <span data-ttu-id="d89ce-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d89ce-110">PARAMETERS</span></span>

### <span data-ttu-id="d89ce-111">-Job</span><span class="sxs-lookup"><span data-stu-id="d89ce-111">-Job</span></span>
<span data-ttu-id="d89ce-112">Указывает объект задания для восстановления сайта, который нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="d89ce-112">Specifies the Site Recovery job object to stop.</span></span>

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

### <span data-ttu-id="d89ce-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d89ce-113">-Name</span></span>
<span data-ttu-id="d89ce-114">Указывает уникальное имя задания для восстановления сайта, которое нужно остановить.</span><span class="sxs-lookup"><span data-stu-id="d89ce-114">Specifies the unique name for the Site Recovery job to stop.</span></span>

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

### <span data-ttu-id="d89ce-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d89ce-115">-DefaultProfile</span></span>
<span data-ttu-id="d89ce-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d89ce-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d89ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d89ce-117">CommonParameters</span></span>
<span data-ttu-id="d89ce-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d89ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d89ce-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d89ce-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d89ce-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d89ce-120">INPUTS</span></span>

### <span data-ttu-id="d89ce-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-121">ASRJob</span></span>
<span data-ttu-id="d89ce-122">Параметр "задание" принимает значение типа "ASRJob" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d89ce-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="d89ce-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d89ce-123">OUTPUTS</span></span>

### <span data-ttu-id="d89ce-124">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d89ce-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d89ce-125">NOTES</span></span>

## <span data-ttu-id="d89ce-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d89ce-126">RELATED LINKS</span></span>

[<span data-ttu-id="d89ce-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="d89ce-128">Restarting-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-128">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="d89ce-129">Возобновить — AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="d89ce-129">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)
