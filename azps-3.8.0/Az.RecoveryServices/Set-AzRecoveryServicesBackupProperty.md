---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 538fe4fe21394c817b7bb2a954fbdbcc2ccfb097
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073525"
---
# <span data-ttu-id="7f852-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7f852-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="7f852-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f852-102">SYNOPSIS</span></span>
<span data-ttu-id="7f852-103">Задает свойства для управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="7f852-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="7f852-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f852-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>
 [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f852-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f852-105">DESCRIPTION</span></span>
<span data-ttu-id="7f852-106">Командлет **Set-AzRecoveryServicesBackupProperty** задает свойства хранилища резервных копий для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="7f852-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="7f852-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f852-107">EXAMPLES</span></span>

### <span data-ttu-id="7f852-108">Пример 1: Настройка хранилища геоизбыточных данных для хранилища</span><span class="sxs-lookup"><span data-stu-id="7f852-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="7f852-109">Первая команда получает хранилище с именем TestVault и сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="7f852-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="7f852-110">Вторая команда задает резервирование хранилища резервных копий для $Vault 01 до геоизбыточной.</span><span class="sxs-lookup"><span data-stu-id="7f852-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="7f852-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f852-111">PARAMETERS</span></span>

### <span data-ttu-id="7f852-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="7f852-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="7f852-113">Указывает тип резервирования резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="7f852-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f852-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f852-114">-DefaultProfile</span></span>
<span data-ttu-id="7f852-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f852-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f852-116">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="7f852-116">-Vault</span></span>
<span data-ttu-id="7f852-117">Указывает имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7f852-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="7f852-118">Хранилище должно быть объектом **AzureRmRecoveryServicesVault** .</span><span class="sxs-lookup"><span data-stu-id="7f852-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f852-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f852-119">-Confirm</span></span>
<span data-ttu-id="7f852-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7f852-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f852-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f852-121">-WhatIf</span></span>
<span data-ttu-id="7f852-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7f852-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7f852-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7f852-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f852-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f852-124">CommonParameters</span></span>
<span data-ttu-id="7f852-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f852-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f852-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f852-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f852-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f852-127">INPUTS</span></span>

### <span data-ttu-id="7f852-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="7f852-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7f852-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f852-129">OUTPUTS</span></span>

### <span data-ttu-id="7f852-130">System. void</span><span class="sxs-lookup"><span data-stu-id="7f852-130">System.Void</span></span>

## <span data-ttu-id="7f852-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f852-131">NOTES</span></span>

## <span data-ttu-id="7f852-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f852-132">RELATED LINKS</span></span>

[<span data-ttu-id="7f852-133">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="7f852-133">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="7f852-134">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7f852-134">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


