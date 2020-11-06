---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/remove-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 88b6b83f24edb06871fd87f61fec1732893b0f41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557148"
---
# <span data-ttu-id="b141b-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b141b-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="b141b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b141b-102">SYNOPSIS</span></span>
<span data-ttu-id="b141b-103">Удаление поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b141b-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b141b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b141b-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b141b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b141b-105">DESCRIPTION</span></span>
<span data-ttu-id="b141b-106">Командлет **Remove-AzureRmSiteRecoveryServicesProvider** удаляет из хранилища поставщик служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b141b-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="b141b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b141b-107">EXAMPLES</span></span>

## <span data-ttu-id="b141b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b141b-108">PARAMETERS</span></span>

### <span data-ttu-id="b141b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b141b-109">-DefaultProfile</span></span>
<span data-ttu-id="b141b-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b141b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b141b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b141b-111">-Force</span></span>
<span data-ttu-id="b141b-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b141b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b141b-113">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b141b-113">-ServicesProvider</span></span>
<span data-ttu-id="b141b-114">Указывает объект поставщика служб.</span><span class="sxs-lookup"><span data-stu-id="b141b-114">Specifies the Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b141b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b141b-115">-Confirm</span></span>
<span data-ttu-id="b141b-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b141b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b141b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b141b-117">-WhatIf</span></span>
<span data-ttu-id="b141b-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b141b-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b141b-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b141b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b141b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b141b-120">CommonParameters</span></span>
<span data-ttu-id="b141b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b141b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b141b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b141b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b141b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b141b-123">INPUTS</span></span>

### <span data-ttu-id="b141b-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b141b-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="b141b-125">Параметр "ServicesProvider" принимает значение типа "ASRRecoveryServicesProvider" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b141b-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="b141b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b141b-126">OUTPUTS</span></span>

### <span data-ttu-id="b141b-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b141b-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b141b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b141b-128">NOTES</span></span>

## <span data-ttu-id="b141b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b141b-129">RELATED LINKS</span></span>

[<span data-ttu-id="b141b-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b141b-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="b141b-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b141b-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
