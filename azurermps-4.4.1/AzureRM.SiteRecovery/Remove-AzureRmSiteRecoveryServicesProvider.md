---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 2FB62869-FF83-4D92-B08B-07AF3C393159
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e7ee32974ef87b86d443d90b7dc628f9c9f1072f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562091"
---
# <span data-ttu-id="805b6-101">Remove-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="805b6-101">Remove-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="805b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="805b6-102">SYNOPSIS</span></span>
<span data-ttu-id="805b6-103">Удаление поставщика служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="805b6-103">Removes an Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="805b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="805b6-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="805b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="805b6-105">DESCRIPTION</span></span>
<span data-ttu-id="805b6-106">Командлет **Remove-AzureRmSiteRecoveryServicesProvider** удаляет из хранилища поставщик служб Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="805b6-106">The **Remove-AzureRmSiteRecoveryServicesProvider** cmdlet removes an Azure Site Recovery Services Provider from the vault.</span></span>

## <span data-ttu-id="805b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="805b6-107">EXAMPLES</span></span>

## <span data-ttu-id="805b6-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="805b6-108">PARAMETERS</span></span>

### <span data-ttu-id="805b6-109">-Force</span><span class="sxs-lookup"><span data-stu-id="805b6-109">-Force</span></span>
<span data-ttu-id="805b6-110">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="805b6-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="805b6-111">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="805b6-111">-ServicesProvider</span></span>
<span data-ttu-id="805b6-112">Указывает объект поставщика служб.</span><span class="sxs-lookup"><span data-stu-id="805b6-112">Specifies the Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="805b6-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="805b6-113">-Confirm</span></span>
<span data-ttu-id="805b6-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="805b6-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="805b6-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="805b6-115">-WhatIf</span></span>
<span data-ttu-id="805b6-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="805b6-116">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="805b6-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="805b6-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="805b6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="805b6-118">-DefaultProfile</span></span>
<span data-ttu-id="805b6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="805b6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="805b6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="805b6-120">CommonParameters</span></span>
<span data-ttu-id="805b6-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="805b6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="805b6-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="805b6-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="805b6-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="805b6-123">INPUTS</span></span>

### <span data-ttu-id="805b6-124">ASRRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="805b6-124">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="805b6-125">Параметр "ServicesProvider" принимает значение типа "ASRRecoveryServicesProvider" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="805b6-125">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="805b6-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="805b6-126">OUTPUTS</span></span>

### <span data-ttu-id="805b6-127">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. SiteRecovery. ASRJob, Microsoft. Azure. Commands. SiteRecovery, Version = 2.0.1.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="805b6-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRJob, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="805b6-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="805b6-128">NOTES</span></span>

## <span data-ttu-id="805b6-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="805b6-129">RELATED LINKS</span></span>

[<span data-ttu-id="805b6-130">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="805b6-130">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="805b6-131">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="805b6-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
