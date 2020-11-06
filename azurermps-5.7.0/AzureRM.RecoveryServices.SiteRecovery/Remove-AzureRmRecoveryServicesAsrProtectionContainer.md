---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 496eeed8b4ed4b41ce2c67d47fc636711cd5cb84
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563424"
---
# <span data-ttu-id="f7f20-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f7f20-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="f7f20-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7f20-102">SYNOPSIS</span></span>
<span data-ttu-id="f7f20-103">Удаляет указанный контейнер защиты из его структуры.</span><span class="sxs-lookup"><span data-stu-id="f7f20-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7f20-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7f20-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7f20-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7f20-105">DESCRIPTION</span></span>
<span data-ttu-id="f7f20-106">Командлет Remove-AzureRmRecoveryServicesAsrProtectionContainer удаляет указанный контейнер защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f7f20-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="f7f20-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7f20-107">EXAMPLES</span></span>

### <span data-ttu-id="f7f20-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7f20-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="f7f20-109">Запускает удаление указанного контейнера защиты и возвращает задание ASR, используемое для отслеживания операции удаления.</span><span class="sxs-lookup"><span data-stu-id="f7f20-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="f7f20-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7f20-110">PARAMETERS</span></span>

### <span data-ttu-id="f7f20-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7f20-111">-Confirm</span></span>
<span data-ttu-id="f7f20-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7f20-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7f20-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7f20-113">-DefaultProfile</span></span>
<span data-ttu-id="f7f20-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7f20-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7f20-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7f20-115">-InputObject</span></span>
<span data-ttu-id="f7f20-116">Указывает контейнер защиты, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f7f20-116">Specifies the protection container to be removed .</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7f20-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7f20-117">-WhatIf</span></span>
<span data-ttu-id="f7f20-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7f20-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7f20-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7f20-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7f20-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7f20-120">CommonParameters</span></span>
<span data-ttu-id="f7f20-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7f20-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7f20-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7f20-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7f20-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7f20-123">INPUTS</span></span>

### <span data-ttu-id="f7f20-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="f7f20-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="f7f20-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7f20-125">OUTPUTS</span></span>

### <span data-ttu-id="f7f20-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f7f20-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f7f20-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7f20-127">NOTES</span></span>

## <span data-ttu-id="f7f20-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7f20-128">RELATED LINKS</span></span>
