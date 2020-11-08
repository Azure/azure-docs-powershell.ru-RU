---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 8d0ecda3c93ac20205cac0ea8bc406a218065a81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066075"
---
# <span data-ttu-id="27ed9-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="27ed9-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="27ed9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="27ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="27ed9-103">Отменяет регистрацию сервера SCDPM или резервного сервера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="27ed9-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="27ed9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="27ed9-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="27ed9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="27ed9-106">Командлет **Unregister-AzRecoveryServicesBackupManagementServer** отменяет регистрацию сервера System Center Data Protection Manager (SCDPM) или резервного сервера Azure из хранилища.</span><span class="sxs-lookup"><span data-stu-id="27ed9-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="27ed9-107">Этот командлет удаляет ссылки на серверы, которые не зарегистрированы в хранилище.</span><span class="sxs-lookup"><span data-stu-id="27ed9-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="27ed9-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="27ed9-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="27ed9-109">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="27ed9-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="27ed9-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="27ed9-110">EXAMPLES</span></span>

### <span data-ttu-id="27ed9-111">Пример 1: Отмена регистрации сервера SCDPM в хранилище</span><span class="sxs-lookup"><span data-stu-id="27ed9-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="27ed9-112">Первая команда получает сервер управления архивацией с именем dpmserver01.contoso.com и сохраняет его в переменной $BMS.</span><span class="sxs-lookup"><span data-stu-id="27ed9-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="27ed9-113">Вторая команда отменяет регистрацию сервера SCDPM в хранилище.</span><span class="sxs-lookup"><span data-stu-id="27ed9-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="27ed9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="27ed9-114">PARAMETERS</span></span>

### <span data-ttu-id="27ed9-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="27ed9-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="27ed9-116">Контейнер резервного копирования служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="27ed9-116">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27ed9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27ed9-117">-DefaultProfile</span></span>
<span data-ttu-id="27ed9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="27ed9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27ed9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27ed9-119">-PassThru</span></span>
<span data-ttu-id="27ed9-120">Верните сервер управления архивацией, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="27ed9-120">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="27ed9-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="27ed9-121">-VaultId</span></span>
<span data-ttu-id="27ed9-122">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="27ed9-122">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27ed9-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27ed9-123">-Confirm</span></span>
<span data-ttu-id="27ed9-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="27ed9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27ed9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27ed9-125">-WhatIf</span></span>
<span data-ttu-id="27ed9-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="27ed9-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27ed9-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="27ed9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27ed9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27ed9-128">CommonParameters</span></span>
<span data-ttu-id="27ed9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="27ed9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27ed9-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27ed9-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27ed9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="27ed9-131">INPUTS</span></span>

### <span data-ttu-id="27ed9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="27ed9-132">System.String</span></span>

## <span data-ttu-id="27ed9-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="27ed9-133">OUTPUTS</span></span>

### <span data-ttu-id="27ed9-134">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="27ed9-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="27ed9-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="27ed9-135">NOTES</span></span>

## <span data-ttu-id="27ed9-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="27ed9-136">RELATED LINKS</span></span>

[<span data-ttu-id="27ed9-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="27ed9-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


