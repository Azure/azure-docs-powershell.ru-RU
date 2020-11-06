---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 0cc4a1c58349157024f38bce6e5ee2d8bcaa3cd5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568427"
---
# <span data-ttu-id="caa01-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="caa01-101">Remove-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="caa01-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="caa01-102">SYNOPSIS</span></span>
<span data-ttu-id="caa01-103">Удаляет указанный контейнер защиты из его структуры.</span><span class="sxs-lookup"><span data-stu-id="caa01-103">Deletes the specified Protection Container from its Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa01-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="caa01-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caa01-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa01-105">DESCRIPTION</span></span>
<span data-ttu-id="caa01-106">Командлет Remove-AzureRmRecoveryServicesAsrProtectionContainer удаляет указанный контейнер защиты Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="caa01-106">The Remove-AzureRmRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="caa01-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="caa01-107">EXAMPLES</span></span>

### <span data-ttu-id="caa01-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="caa01-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzureRmRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="caa01-109">Запускает удаление указанного контейнера защиты и возвращает задание ASR, используемое для отслеживания операции удаления.</span><span class="sxs-lookup"><span data-stu-id="caa01-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="caa01-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="caa01-110">PARAMETERS</span></span>

### <span data-ttu-id="caa01-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa01-111">-DefaultProfile</span></span>
<span data-ttu-id="caa01-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="caa01-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="caa01-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="caa01-113">-InputObject</span></span>
<span data-ttu-id="caa01-114">Указывает контейнер защиты, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="caa01-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="caa01-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="caa01-115">-Confirm</span></span>
<span data-ttu-id="caa01-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="caa01-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa01-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa01-117">-WhatIf</span></span>
<span data-ttu-id="caa01-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="caa01-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa01-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="caa01-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa01-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa01-120">CommonParameters</span></span>
<span data-ttu-id="caa01-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="caa01-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa01-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa01-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa01-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="caa01-123">INPUTS</span></span>

### <span data-ttu-id="caa01-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="caa01-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="caa01-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="caa01-125">OUTPUTS</span></span>

### <span data-ttu-id="caa01-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="caa01-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="caa01-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="caa01-127">NOTES</span></span>

## <span data-ttu-id="caa01-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="caa01-128">RELATED LINKS</span></span>
