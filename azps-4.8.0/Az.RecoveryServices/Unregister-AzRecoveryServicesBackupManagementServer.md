---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: cc52435ff0b288656e4a917620659737f33916ca
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079360"
---
# <span data-ttu-id="55e3b-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55e3b-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="55e3b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="55e3b-103">Отменяет регистрацию сервера SCDPM или резервного сервера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="55e3b-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="55e3b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55e3b-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="55e3b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="55e3b-106">Командлет **Unregister-AzRecoveryServicesBackupManagementServer** отменяет регистрацию сервера System Center Data Protection Manager (SCDPM) или резервного сервера Azure из хранилища.</span><span class="sxs-lookup"><span data-stu-id="55e3b-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="55e3b-107">Этот командлет удаляет ссылки на серверы, которые не зарегистрированы в хранилище.</span><span class="sxs-lookup"><span data-stu-id="55e3b-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="55e3b-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="55e3b-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="55e3b-109">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="55e3b-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="55e3b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55e3b-110">EXAMPLES</span></span>

### <span data-ttu-id="55e3b-111">Пример 1: Отмена регистрации сервера SCDPM в хранилище</span><span class="sxs-lookup"><span data-stu-id="55e3b-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```powershell
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="55e3b-112">Первая команда получает сервер управления архивацией с именем dpmserver01.contoso.com и сохраняет его в переменной $BMS.</span><span class="sxs-lookup"><span data-stu-id="55e3b-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="55e3b-113">Вторая команда отменяет регистрацию сервера SCDPM в хранилище.</span><span class="sxs-lookup"><span data-stu-id="55e3b-113">The second command unregisters the SCDPM server from the vault.</span></span>

### <span data-ttu-id="55e3b-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="55e3b-114">Example 2</span></span>

<span data-ttu-id="55e3b-115">Отменяет регистрацию сервера SCDPM или резервного сервера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="55e3b-115">Unregisters a SCDPM server or Backup server from the vault.</span></span> <span data-ttu-id="55e3b-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="55e3b-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Unregister-AzRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer <BackupEngineBase> -VaultId $vault.ID
```

## <span data-ttu-id="55e3b-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55e3b-117">PARAMETERS</span></span>

### <span data-ttu-id="55e3b-118">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55e3b-118">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="55e3b-119">Контейнер резервного копирования служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="55e3b-119">The recovery services backup container.</span></span>

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

### <span data-ttu-id="55e3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e3b-120">-DefaultProfile</span></span>
<span data-ttu-id="55e3b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55e3b-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55e3b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55e3b-122">-PassThru</span></span>
<span data-ttu-id="55e3b-123">Верните сервер управления архивацией, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="55e3b-123">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="55e3b-124">-VaultId</span><span class="sxs-lookup"><span data-stu-id="55e3b-124">-VaultId</span></span>
<span data-ttu-id="55e3b-125">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="55e3b-125">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="55e3b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55e3b-126">-Confirm</span></span>
<span data-ttu-id="55e3b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55e3b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55e3b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55e3b-128">-WhatIf</span></span>
<span data-ttu-id="55e3b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55e3b-129">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="55e3b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e3b-130">CommonParameters</span></span>
<span data-ttu-id="55e3b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55e3b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e3b-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55e3b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e3b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55e3b-133">INPUTS</span></span>

### <span data-ttu-id="55e3b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="55e3b-134">System.String</span></span>

## <span data-ttu-id="55e3b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55e3b-135">OUTPUTS</span></span>

### <span data-ttu-id="55e3b-136">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="55e3b-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="55e3b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="55e3b-137">NOTES</span></span>

## <span data-ttu-id="55e3b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55e3b-138">RELATED LINKS</span></span>

[<span data-ttu-id="55e3b-139">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="55e3b-139">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


