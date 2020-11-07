---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B1D914F8-4181-4BF1-B1D3-A5857DA8254C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryProtectionContainerMapping.md
ms.openlocfilehash: a0de6cc5594b019275cb14785cbae3b969d44301
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732682"
---
# <span data-ttu-id="0899b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0899b-101">Remove-AzureRmSiteRecoveryProtectionContainerMapping</span></span>

## <span data-ttu-id="0899b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0899b-102">SYNOPSIS</span></span>
<span data-ttu-id="0899b-103">Удаляет сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0899b-103">Removes an Azure Site Recovery Protection Container mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0899b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0899b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryProtectionContainerMapping
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0899b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0899b-105">DESCRIPTION</span></span>
<span data-ttu-id="0899b-106">Командлет **Remove-AzureRmSiteRecoveryProtectionContainerMapping** удаляет сопоставление контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0899b-106">The **Remove-AzureRmSiteRecoveryProtectionContainerMapping** cmdlet removes an Azure Site Recovery Protection Container mapping.</span></span>

## <span data-ttu-id="0899b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0899b-107">EXAMPLES</span></span>

## <span data-ttu-id="0899b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0899b-108">PARAMETERS</span></span>

### <span data-ttu-id="0899b-109">-Force</span><span class="sxs-lookup"><span data-stu-id="0899b-109">-Force</span></span>
<span data-ttu-id="0899b-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0899b-110">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0899b-111">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0899b-111">-ProtectionContainerMapping</span></span>
<span data-ttu-id="0899b-112">Указывает объект сопоставления контейнера защиты для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0899b-112">Specifies the Azure Site Recovery Protection Container mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0899b-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0899b-113">-Confirm</span></span>
<span data-ttu-id="0899b-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0899b-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0899b-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0899b-115">-WhatIf</span></span>
<span data-ttu-id="0899b-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0899b-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="0899b-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0899b-117">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0899b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0899b-118">-DefaultProfile</span></span>
<span data-ttu-id="0899b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0899b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0899b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0899b-120">CommonParameters</span></span>
<span data-ttu-id="0899b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0899b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0899b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0899b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0899b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0899b-123">INPUTS</span></span>

### <span data-ttu-id="0899b-124">ASRProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0899b-124">ASRProtectionContainerMapping</span></span>
<span data-ttu-id="0899b-125">Параметр "ProtectionContainerMapping" принимает значение типа "ASRProtectionContainerMapping" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="0899b-125">Parameter 'ProtectionContainerMapping' accepts value of type 'ASRProtectionContainerMapping' from the pipeline</span></span>

## <span data-ttu-id="0899b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0899b-126">OUTPUTS</span></span>

### <span data-ttu-id="0899b-127">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0899b-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0899b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0899b-128">NOTES</span></span>

## <span data-ttu-id="0899b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0899b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0899b-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0899b-130">Get-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./Get-AzureRmSiteRecoveryProtectionContainerMapping.md)

[<span data-ttu-id="0899b-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="0899b-131">New-AzureRmSiteRecoveryProtectionContainerMapping</span></span>](./New-AzureRmSiteRecoveryProtectionContainerMapping.md)
