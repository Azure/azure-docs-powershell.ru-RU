---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733644"
---
# <span data-ttu-id="1e500-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1e500-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="1e500-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e500-102">SYNOPSIS</span></span>
<span data-ttu-id="1e500-103">Обновляет (обновить сервер) данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e500-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e500-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e500-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e500-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e500-105">DESCRIPTION</span></span>
<span data-ttu-id="1e500-106">Командлет **Update-AzureRmRecoveryServicesAsrServicesProvider** обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="1e500-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="1e500-107">Этот командлет можно использовать для активации обновления данных, полученных от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="1e500-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="1e500-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e500-108">EXAMPLES</span></span>

### <span data-ttu-id="1e500-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e500-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

<span data-ttu-id="1e500-110">Запускает операцию обновления данных, предоставленных указанным поставщиком служб ASR, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="1e500-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span> 

## <span data-ttu-id="1e500-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e500-111">PARAMETERS</span></span>

### <span data-ttu-id="1e500-112">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e500-112">-InputObject</span></span>
<span data-ttu-id="1e500-113">Объект input: определяет объект поставщика служб ASR, соответствующий поставщику служб ASR, который идентифицирует сервер, сведения о котором были обновлены (обновлены.)</span><span class="sxs-lookup"><span data-stu-id="1e500-113">Input Object: Specifies the ASR services provider object corresponding to the ASR services provider that identifies the server for which information is to updated(refreshed.)</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e500-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e500-114">-Confirm</span></span>
<span data-ttu-id="1e500-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e500-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e500-116">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e500-116">-WhatIf</span></span>
<span data-ttu-id="1e500-117">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e500-117">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e500-118">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e500-118">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e500-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e500-119">CommonParameters</span></span>
<span data-ttu-id="1e500-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e500-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e500-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e500-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e500-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e500-122">INPUTS</span></span>

### <span data-ttu-id="1e500-123">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1e500-123">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="1e500-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e500-124">OUTPUTS</span></span>

### <span data-ttu-id="1e500-125">System. Object</span><span class="sxs-lookup"><span data-stu-id="1e500-125">System.Object</span></span>

## <span data-ttu-id="1e500-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e500-126">NOTES</span></span>

## <span data-ttu-id="1e500-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e500-127">RELATED LINKS</span></span>

[<span data-ttu-id="1e500-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1e500-128">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="1e500-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="1e500-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
