---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: 27c90687b212c0ed41dcb080df1be5686a876725
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733962"
---
# <span data-ttu-id="d097f-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d097f-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="d097f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d097f-102">SYNOPSIS</span></span>
<span data-ttu-id="d097f-103">Удаляет сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d097f-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d097f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d097f-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d097f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d097f-105">DESCRIPTION</span></span>
<span data-ttu-id="d097f-106">Командлет **Remove-AzureRmSiteRecoveryProtectionContainerMapping** удаляет сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d097f-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="d097f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d097f-107">EXAMPLES</span></span>

## <span data-ttu-id="d097f-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d097f-108">PARAMETERS</span></span>

### <span data-ttu-id="d097f-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d097f-109">-DefaultProfile</span></span>
<span data-ttu-id="d097f-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d097f-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d097f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d097f-111">-Force</span></span>
<span data-ttu-id="d097f-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d097f-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097f-113">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d097f-113">-ProtectionContainerMapping</span></span>
<span data-ttu-id="d097f-114">Указывает объект сопоставления контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="d097f-114">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d097f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d097f-115">-Confirm</span></span>
<span data-ttu-id="d097f-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d097f-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d097f-117">-WhatIf</span></span>
<span data-ttu-id="d097f-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d097f-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d097f-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d097f-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d097f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d097f-120">CommonParameters</span></span>
<span data-ttu-id="d097f-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d097f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d097f-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d097f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d097f-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d097f-123">INPUTS</span></span>

### <span data-ttu-id="d097f-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d097f-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="d097f-125">Параметр "ProtectionContainerMapping" принимает значение типа "ASRProtectionContainerMapping" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d097f-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="d097f-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d097f-126">OUTPUTS</span></span>

### <span data-ttu-id="d097f-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d097f-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d097f-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="d097f-128">NOTES</span></span>

## <span data-ttu-id="d097f-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d097f-129">RELATED LINKS</span></span>

[<span data-ttu-id="d097f-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d097f-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="d097f-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d097f-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
