---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 70CF4CA5-F456-4953-87E5-12B5CBDE6D52
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryprotectionentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 21bf19ba4a4d17ef41f6741deedd5cac486bbb32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732510"
---
# <span data-ttu-id="5e58c-101">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e58c-101">Set-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="5e58c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5e58c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e58c-103">Задает состояние для элемента защиты восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e58c-103">Sets the state for a Site Recovery protection entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e58c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5e58c-104">SYNTAX</span></span>

### <span data-ttu-id="5e58c-105">Отключение (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5e58c-105">DisableDR (Default)</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e58c-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="5e58c-106">EnterpriseToEnterprise</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e58c-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="5e58c-107">EnterpriseToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> [-WaitForCompletion] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e58c-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="5e58c-108">HyperVSiteToAzure</span></span>
```
Set-AzureRmSiteRecoveryProtectionEntity -ProtectionEntity <ASRProtectionEntity> -Protection <String>
 -Policy <ASRPolicy> -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String>
 [-WaitForCompletion] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5e58c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e58c-109">DESCRIPTION</span></span>
<span data-ttu-id="5e58c-110">Командлет **Set-AzureRmSiteRecoveryProtectionEntity** включает или выключает защиту для сущности "Защита Azure Site Recovery".</span><span class="sxs-lookup"><span data-stu-id="5e58c-110">The **Set-AzureRmSiteRecoveryProtectionEntity** cmdlet enables or disables protection on an Azure Site Recovery protection entity.</span></span>

## <span data-ttu-id="5e58c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5e58c-111">EXAMPLES</span></span>

## <span data-ttu-id="5e58c-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5e58c-112">PARAMETERS</span></span>

### <span data-ttu-id="5e58c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e58c-113">-DefaultProfile</span></span>
<span data-ttu-id="5e58c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5e58c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e58c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5e58c-115">-Force</span></span>
<span data-ttu-id="5e58c-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="5e58c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5e58c-117">-OS</span><span class="sxs-lookup"><span data-stu-id="5e58c-117">-OS</span></span>
<span data-ttu-id="5e58c-118">Указывает тип операционной системы.</span><span class="sxs-lookup"><span data-stu-id="5e58c-118">Specifies the operating system type.</span></span>
<span data-ttu-id="5e58c-119">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5e58c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e58c-120">Windows</span><span class="sxs-lookup"><span data-stu-id="5e58c-120">Windows</span></span>
- <span data-ttu-id="5e58c-121">Linux</span><span class="sxs-lookup"><span data-stu-id="5e58c-121">Linux</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-122">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="5e58c-122">-OSDiskName</span></span>
<span data-ttu-id="5e58c-123">Указывает имя диска, который содержит операционную систему.</span><span class="sxs-lookup"><span data-stu-id="5e58c-123">Specifies the name of the disk that contains the operating system.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-124">-Policy (политика)</span><span class="sxs-lookup"><span data-stu-id="5e58c-124">-Policy</span></span>
<span data-ttu-id="5e58c-125">Указывает объект политики восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5e58c-125">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-126">-Защита</span><span class="sxs-lookup"><span data-stu-id="5e58c-126">-Protection</span></span>
<span data-ttu-id="5e58c-127">Указывает, следует ли включить или отключить защиту.</span><span class="sxs-lookup"><span data-stu-id="5e58c-127">Specifies whether protection should be enabled or disabled.</span></span>
<span data-ttu-id="5e58c-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5e58c-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e58c-129">Включите</span><span class="sxs-lookup"><span data-stu-id="5e58c-129">Enable</span></span>
- <span data-ttu-id="5e58c-130">Ключив</span><span class="sxs-lookup"><span data-stu-id="5e58c-130">Disable</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-131">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e58c-131">-ProtectionEntity</span></span>
<span data-ttu-id="5e58c-132">Указывает объект сущности для защиты.</span><span class="sxs-lookup"><span data-stu-id="5e58c-132">Specifies the protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-133">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5e58c-133">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="5e58c-134">Указывает идентификатор целевой учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="5e58c-134">Specifies the ID of the target Azure Storage account.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e58c-135">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5e58c-135">-WaitForCompletion</span></span>
<span data-ttu-id="5e58c-136">Указывает на то, что команда ожидает завершения перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="5e58c-136">Indicates that the command waits for completion before returning.</span></span>

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

### <span data-ttu-id="5e58c-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5e58c-137">-Confirm</span></span>
<span data-ttu-id="5e58c-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5e58c-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e58c-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e58c-139">-WhatIf</span></span>
<span data-ttu-id="5e58c-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5e58c-140">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="5e58c-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5e58c-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e58c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e58c-142">CommonParameters</span></span>
<span data-ttu-id="5e58c-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5e58c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e58c-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e58c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e58c-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5e58c-145">INPUTS</span></span>

### <span data-ttu-id="5e58c-146">ASRProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e58c-146">ASRProtectionEntity</span></span>
<span data-ttu-id="5e58c-147">Параметр "ProtectionEntity" принимает значение типа "ASRProtectionEntity" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="5e58c-147">Parameter 'ProtectionEntity' accepts value of type 'ASRProtectionEntity' from the pipeline</span></span>

## <span data-ttu-id="5e58c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5e58c-148">OUTPUTS</span></span>

### <span data-ttu-id="5e58c-149">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e58c-149">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e58c-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="5e58c-150">NOTES</span></span>

## <span data-ttu-id="5e58c-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5e58c-151">RELATED LINKS</span></span>

[<span data-ttu-id="5e58c-152">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5e58c-152">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)
