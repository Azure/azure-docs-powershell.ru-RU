---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C635D723-0F03-4EF8-9435-24DBE0859899
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 17187a1a5caa2de3f39ad7153ee1313e4ee8e3e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225369"
---
# <span data-ttu-id="73e71-101">Set-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="73e71-101">Set-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="73e71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73e71-102">SYNOPSIS</span></span>
<span data-ttu-id="73e71-103">Задает свойства для управления резервными копиями.</span><span class="sxs-lookup"><span data-stu-id="73e71-103">Sets the properties for backup management.</span></span>

## <span data-ttu-id="73e71-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73e71-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesBackupProperty -Vault <ARSVault>  [-BackupStorageRedundancy <AzureRmRecoveryServicesBackupStorageRedundancyType>]
 [-EnableCrossRegionRestore] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73e71-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73e71-105">DESCRIPTION</span></span>
<span data-ttu-id="73e71-106">**Cmdlet Set-AzRecoveryServicesBackupProperty** задает свойства резервного копирования хранилища для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="73e71-106">The **Set-AzRecoveryServicesBackupProperty** cmdlet sets backup storage properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="73e71-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73e71-107">EXAMPLES</span></span>

### <span data-ttu-id="73e71-108">Пример 1. Настройка geoRedundant storage для хранилища</span><span class="sxs-lookup"><span data-stu-id="73e71-108">Example 1: Set GeoRedundant storage for a vault</span></span>
```
PS C:\> $Vault01 = Get-AzRecoveryServicesVault -Name "TestVault"
PS C:\> Set-AzRecoveryServicesBackupProperty -Vault $Vault01 -BackupStorageRedundancy GeoRedundant
```

<span data-ttu-id="73e71-109">Первая команда получает хранилище TestVault, а затем сохраняет его в переменной $Vault 01.</span><span class="sxs-lookup"><span data-stu-id="73e71-109">The first command gets the vault named TestVault, and then stores it in the $Vault01 variable.</span></span>
<span data-ttu-id="73e71-110">Вторая команда задает избыточность резервного хранилища для $Vault 01 в geoRedundant.</span><span class="sxs-lookup"><span data-stu-id="73e71-110">The second command sets the backup storage redundancy for $Vault01 to GeoRedundant.</span></span>

## <span data-ttu-id="73e71-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73e71-111">PARAMETERS</span></span>

### <span data-ttu-id="73e71-112">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="73e71-112">-BackupStorageRedundancy</span></span>
<span data-ttu-id="73e71-113">Определяет тип избыточности резервного хранилища.</span><span class="sxs-lookup"><span data-stu-id="73e71-113">Specifies the backup storage redundancy type.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.RecoveryServices.AzureRmRecoveryServicesBackupStorageRedundancyType]
Parameter Sets: (All)
Aliases:
Accepted values: GeoRedundant, ZoneRedundant, LocallyRedundant

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73e71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73e71-114">-DefaultProfile</span></span>
<span data-ttu-id="73e71-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73e71-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73e71-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="73e71-116">-Vault</span></span>
<span data-ttu-id="73e71-117">Указывает имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="73e71-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="73e71-118">Хранилище должно быть **объектом AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="73e71-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="73e71-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73e71-119">-Confirm</span></span>
<span data-ttu-id="73e71-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73e71-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73e71-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73e71-121">-WhatIf</span></span>
<span data-ttu-id="73e71-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73e71-122">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="73e71-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73e71-123">CommonParameters</span></span>
<span data-ttu-id="73e71-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73e71-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73e71-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73e71-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73e71-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73e71-126">INPUTS</span></span>

### <span data-ttu-id="73e71-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="73e71-127">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="73e71-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73e71-128">OUTPUTS</span></span>

### <span data-ttu-id="73e71-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="73e71-129">System.Void</span></span>

## <span data-ttu-id="73e71-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73e71-130">NOTES</span></span>

## <span data-ttu-id="73e71-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73e71-131">RELATED LINKS</span></span>

[<span data-ttu-id="73e71-132">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="73e71-132">Get-AzRecoveryServicesBackupProperty</span></span>](./Get-AzRecoveryServicesBackupProperty.md)

[<span data-ttu-id="73e71-133">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="73e71-133">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)


