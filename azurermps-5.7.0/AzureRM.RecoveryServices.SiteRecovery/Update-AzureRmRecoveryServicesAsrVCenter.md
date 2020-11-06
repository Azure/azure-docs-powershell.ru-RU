---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 298443c4b962a2be6c5cf3849657d0fe8bbaf978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558860"
---
# <span data-ttu-id="87462-101">Update-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="87462-101">Update-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="87462-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="87462-102">SYNOPSIS</span></span>
<span data-ttu-id="87462-103">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="87462-103">Update discovery details for a registered vCenter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87462-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="87462-104">SYNTAX</span></span>

### <span data-ttu-id="87462-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="87462-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-Account <ASRRunAsAccount>] [-Port <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87462-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="87462-106">ByResourceId</span></span>
```
Update-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87462-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="87462-107">DESCRIPTION</span></span>
<span data-ttu-id="87462-108">Командлет **Update-AzureRmRecoveryServicesAsrvCenter** обновляет сведения о обнаружении зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="87462-108">The **Update-AzureRmRecoveryServicesAsrvCenter** cmdlet is updates discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="87462-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="87462-109">EXAMPLES</span></span>

### <span data-ttu-id="87462-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="87462-110">Example 1</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrvCenter -Account $fabric.fabricSpecificDetails.RunAsAccounts[1] -InputObject $vCenter
Returns ASRJOB for update vCenter.
```

<span data-ttu-id="87462-111">Обновите сведения о обнаружении для зарегистрированного vCenter.</span><span class="sxs-lookup"><span data-stu-id="87462-111">Update discovery details for a registered vCenter.</span></span>

## <span data-ttu-id="87462-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="87462-112">PARAMETERS</span></span>

### <span data-ttu-id="87462-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="87462-113">-Account</span></span>
<span data-ttu-id="87462-114">учетные данные для входа в vCenter.</span><span class="sxs-lookup"><span data-stu-id="87462-114">vCenter login credentials account.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87462-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="87462-115">-Confirm</span></span>
<span data-ttu-id="87462-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="87462-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87462-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87462-117">-DefaultProfile</span></span>
<span data-ttu-id="87462-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="87462-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87462-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87462-119">-InputObject</span></span>
<span data-ttu-id="87462-120">Объект сервера vCenter, для которого нужно обновить сведения о обнаружении.</span><span class="sxs-lookup"><span data-stu-id="87462-120">The vCenter server object to update discovery details for.</span></span>

```yaml
Type: ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87462-121">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="87462-121">-Port</span></span>
<span data-ttu-id="87462-122">Порт TCP на сервере vCenter Server, который будет использоваться для обнаружения.</span><span class="sxs-lookup"><span data-stu-id="87462-122">The TCP port on the vCenter server to use for discovery.</span></span>

```yaml
Type: Int32
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87462-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87462-123">-ResourceId</span></span>
<span data-ttu-id="87462-124">Указывает resourceId для vCenter.</span><span class="sxs-lookup"><span data-stu-id="87462-124">Specifies the resourceId of vCenter.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87462-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87462-125">-WhatIf</span></span>
<span data-ttu-id="87462-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="87462-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87462-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="87462-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87462-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87462-128">CommonParameters</span></span>
<span data-ttu-id="87462-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="87462-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87462-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87462-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87462-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="87462-131">INPUTS</span></span>

### <span data-ttu-id="87462-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="87462-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="87462-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="87462-133">OUTPUTS</span></span>

### <span data-ttu-id="87462-134">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="87462-134">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="87462-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="87462-135">NOTES</span></span>

## <span data-ttu-id="87462-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="87462-136">RELATED LINKS</span></span>
