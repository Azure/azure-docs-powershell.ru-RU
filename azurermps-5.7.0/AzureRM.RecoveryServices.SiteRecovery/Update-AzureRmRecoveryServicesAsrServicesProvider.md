---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 823ad4b0f7eff8f80fea012bdef4b3c2662d55e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558863"
---
# <span data-ttu-id="be40a-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="be40a-101">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="be40a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be40a-102">SYNOPSIS</span></span>
<span data-ttu-id="be40a-103">Обновляет (обновить сервер) данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="be40a-103">Refreshes (Refresh server) the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be40a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be40a-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be40a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be40a-105">DESCRIPTION</span></span>
<span data-ttu-id="be40a-106">Командлет **Update-AzureRmRecoveryServicesAsrServicesProvider** обновляет данные, полученные от поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="be40a-106">The **Update-AzureRmRecoveryServicesAsrServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span> <span data-ttu-id="be40a-107">Этот командлет можно использовать для активации обновления данных, полученных от поставщика услуг восстановления.</span><span class="sxs-lookup"><span data-stu-id="be40a-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="be40a-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be40a-108">EXAMPLES</span></span>

### <span data-ttu-id="be40a-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be40a-109">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject $ServicesProvider
```

<span data-ttu-id="be40a-110">Запускает операцию обновления данных, предоставленных указанным поставщиком служб ASR, и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="be40a-110">Starts the operation of refreshing the information from the specified ASR services provider and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="be40a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be40a-111">PARAMETERS</span></span>

### <span data-ttu-id="be40a-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be40a-112">-Confirm</span></span>
<span data-ttu-id="be40a-113">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be40a-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be40a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be40a-114">-DefaultProfile</span></span>
<span data-ttu-id="be40a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="be40a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="be40a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="be40a-116">-InputObject</span></span>
<span data-ttu-id="be40a-117">Указывает объект поставщика служб ASR, который определяет сервер, сведения о котором нужно обновить (обновление.)</span><span class="sxs-lookup"><span data-stu-id="be40a-117">Specifies the ASR services provider object that identifies the server for which information is to updated(refreshed.)</span></span>

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

### <span data-ttu-id="be40a-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be40a-118">-WhatIf</span></span>
<span data-ttu-id="be40a-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be40a-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be40a-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be40a-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be40a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be40a-121">CommonParameters</span></span>
<span data-ttu-id="be40a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be40a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be40a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be40a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be40a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be40a-124">INPUTS</span></span>

### <span data-ttu-id="be40a-125">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="be40a-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider</span></span>

## <span data-ttu-id="be40a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be40a-126">OUTPUTS</span></span>

### <span data-ttu-id="be40a-127">System. Object</span><span class="sxs-lookup"><span data-stu-id="be40a-127">System.Object</span></span>

## <span data-ttu-id="be40a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="be40a-128">NOTES</span></span>

## <span data-ttu-id="be40a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be40a-129">RELATED LINKS</span></span>

[<span data-ttu-id="be40a-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="be40a-130">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="be40a-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="be40a-131">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
