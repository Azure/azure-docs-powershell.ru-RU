---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrvcenter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrVCenter.md
ms.openlocfilehash: 505d2d81eefed3132cd693ea6cd989fde173b8b3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568162"
---
# <span data-ttu-id="3f511-101">Remove-AzureRmRecoveryServicesAsrvCenter</span><span class="sxs-lookup"><span data-stu-id="3f511-101">Remove-AzureRmRecoveryServicesAsrvCenter</span></span>

## <span data-ttu-id="3f511-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f511-102">SYNOPSIS</span></span>
<span data-ttu-id="3f511-103">Удаляет vCenter Server из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="3f511-103">Removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f511-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f511-104">SYNTAX</span></span>

### <span data-ttu-id="3f511-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f511-105">Default (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -InputObject <ASRvCenter> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f511-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3f511-106">ByResourceId</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f511-107">ByName</span><span class="sxs-lookup"><span data-stu-id="3f511-107">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrvCenter -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f511-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f511-108">DESCRIPTION</span></span>
<span data-ttu-id="3f511-109">Командлет **Remove-AzureRmRecoveryServicesAsrvCenter** удаляет сервер vCenter из структуры ASR и останавливает Обнаружение виртуальных машин с сервера vCenter.</span><span class="sxs-lookup"><span data-stu-id="3f511-109">The **Remove-AzureRmRecoveryServicesAsrvCenter** cmdlet removes the vCenter server from the ASR fabric and stops discovery of virtual machines from the vCenter server.</span></span>

## <span data-ttu-id="3f511-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f511-110">EXAMPLES</span></span>

### <span data-ttu-id="3f511-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f511-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesAsrvCenterServer -InputObject $vCenter
```

<span data-ttu-id="3f511-112">Удаляет vCenter Server из структуры ASR.</span><span class="sxs-lookup"><span data-stu-id="3f511-112">Removes the vCenter server from the ASR fabric.</span></span>

## <span data-ttu-id="3f511-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f511-113">PARAMETERS</span></span>

### <span data-ttu-id="3f511-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f511-114">-DefaultProfile</span></span>
<span data-ttu-id="3f511-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3f511-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f511-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="3f511-116">-Fabric</span></span>
<span data-ttu-id="3f511-117">Объект Fabric ASR, представляющий сервер конфигурации.</span><span class="sxs-lookup"><span data-stu-id="3f511-117">ASR fabric object representing the Configuration Server.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f511-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f511-118">-InputObject</span></span>
<span data-ttu-id="3f511-119">Объект ASR vCenter, представляющий сервер vCenter Server, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3f511-119">ASR vCenter object representing the vCenter server to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter
Parameter Sets: Default
Aliases: vCenter

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f511-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f511-120">-Name</span></span>
<span data-ttu-id="3f511-121">Имя сервера vCenter Server.</span><span class="sxs-lookup"><span data-stu-id="3f511-121">Name of the vCenter Server.</span></span>

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

### <span data-ttu-id="3f511-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f511-122">-ResourceId</span></span>
<span data-ttu-id="3f511-123">Указывает ИД ресурса vCenter, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3f511-123">Specifies the resourceId of vCenter to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f511-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f511-124">-Confirm</span></span>
<span data-ttu-id="3f511-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f511-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f511-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f511-126">-WhatIf</span></span>
<span data-ttu-id="3f511-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f511-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f511-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f511-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f511-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f511-129">CommonParameters</span></span>
<span data-ttu-id="3f511-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f511-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f511-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f511-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f511-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f511-132">INPUTS</span></span>

### <span data-ttu-id="3f511-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRvCenter</span><span class="sxs-lookup"><span data-stu-id="3f511-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRvCenter</span></span>

## <span data-ttu-id="3f511-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f511-134">OUTPUTS</span></span>

### <span data-ttu-id="3f511-135">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="3f511-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="3f511-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f511-136">NOTES</span></span>

## <span data-ttu-id="3f511-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f511-137">RELATED LINKS</span></span>
