---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesbackupproperties
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesBackupProperties.md
ms.openlocfilehash: 7fa55bd306a1cbe04ddf3af63a66682a0fa17f1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558332"
---
# <span data-ttu-id="96758-101">Set-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="96758-101">Set-AzureRmRecoveryServicesBackupProperties</span></span>

## <span data-ttu-id="96758-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96758-102">SYNOPSIS</span></span>
<span data-ttu-id="96758-103">Задает свойства для управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="96758-103">Sets the properties for backup management.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96758-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96758-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesBackupProperties -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96758-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96758-105">DESCRIPTION</span></span>
<span data-ttu-id="96758-106">Командлет **Set-AzureRmRecoveryServicesBackupProperties** задает свойства хранилища резервных копий для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="96758-106">The **Set-AzureRmRecoveryServicesBackupProperties** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="96758-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96758-107">EXAMPLES</span></span>

### <span data-ttu-id="96758-108">Пример 1: Настройка хранилища геоизбыточных данных для хранилища</span><span class="sxs-lookup"><span data-stu-id="96758-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzureRmRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzureRmRecoveryServicesBackupProperties -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="96758-109">Первая команда получает хранилище с именем TestVault и сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="96758-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="96758-110">Вторая команда задает резервирование хранилища резервных копий для $Vault 01 до геоизбыточной.</span><span class="sxs-lookup"><span data-stu-id="96758-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="96758-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96758-111">PARAMETERS</span></span>

### <span data-ttu-id="96758-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="96758-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="96758-113">Указывает тип резервирования резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="96758-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: AzureRmRecoveryServicesBackupStorageRedundancyType
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96758-114">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="96758-114">-Vault</span></span>
<span data-ttu-id="96758-115">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="96758-115">Specifies the name of the vault.</span></span>
<span data-ttu-id="96758-116">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="96758-116">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96758-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96758-117">-Confirm</span></span>
<span data-ttu-id="96758-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96758-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96758-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96758-119">-WhatIf</span></span>
<span data-ttu-id="96758-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96758-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96758-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96758-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96758-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96758-122">-DefaultProfile</span></span>
<span data-ttu-id="96758-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96758-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96758-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96758-124">CommonParameters</span></span>
<span data-ttu-id="96758-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96758-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96758-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96758-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96758-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96758-127">INPUTS</span></span>

### <span data-ttu-id="96758-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="96758-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="96758-129">Параметры: хранилище (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96758-129">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="96758-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96758-130">OUTPUTS</span></span>

### <span data-ttu-id="96758-131">System. void</span><span class="sxs-lookup"><span data-stu-id="96758-131">System.Void</span></span>

## <span data-ttu-id="96758-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="96758-132">NOTES</span></span>

## <span data-ttu-id="96758-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96758-133">RELATED LINKS</span></span>

[<span data-ttu-id="96758-134">Get-AzureRmRecoveryServicesBackupProperties</span><span class="sxs-lookup"><span data-stu-id="96758-134">Get-AzureRmRecoveryServicesBackupProperties</span></span>](./Get-AzureRmRecoveryServicesBackupProperties.md)

[<span data-ttu-id="96758-135">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="96758-135">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)


