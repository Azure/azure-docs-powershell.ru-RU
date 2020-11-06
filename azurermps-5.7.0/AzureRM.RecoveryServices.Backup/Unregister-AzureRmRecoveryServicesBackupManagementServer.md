---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/unregister-azurermrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 7612a816db41e3befb58cc739bcc78e2d27ec8d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558895"
---
# <span data-ttu-id="69abc-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="69abc-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="69abc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69abc-102">SYNOPSIS</span></span>
<span data-ttu-id="69abc-103">Отменяет регистрацию сервера SCDPM или резервного сервера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="69abc-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69abc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69abc-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69abc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69abc-105">DESCRIPTION</span></span>
<span data-ttu-id="69abc-106">Командлет **Unregister-AzureRmRecoveryServicesBackupManagementServer** отменяет регистрацию сервера System Center Data Protection Manager (SCDPM) или резервного сервера Azure из хранилища.</span><span class="sxs-lookup"><span data-stu-id="69abc-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="69abc-107">Этот командлет удаляет ссылки на серверы, которые не зарегистрированы в хранилище.</span><span class="sxs-lookup"><span data-stu-id="69abc-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="69abc-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="69abc-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="69abc-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="69abc-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="69abc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69abc-110">EXAMPLES</span></span>

### <span data-ttu-id="69abc-111">Пример 1: Отмена регистрации сервера SCDPM в хранилище</span><span class="sxs-lookup"><span data-stu-id="69abc-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="69abc-112">Первая команда получает сервер управления архивацией с именем dpmserver01.contoso.com и сохраняет его в переменной $BMS.</span><span class="sxs-lookup"><span data-stu-id="69abc-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="69abc-113">Вторая команда отменяет регистрацию сервера SCDPM в хранилище.</span><span class="sxs-lookup"><span data-stu-id="69abc-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="69abc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69abc-114">PARAMETERS</span></span>

### <span data-ttu-id="69abc-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="69abc-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="69abc-116">Указывает объект сервера SCDPM, который нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="69abc-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="69abc-117">Чтобы получить объект **BackupManagementServer** , используйте командлет Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="69abc-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

```yaml
Type: BackupEngineBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69abc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69abc-118">-DefaultProfile</span></span>
<span data-ttu-id="69abc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="69abc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69abc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69abc-120">-PassThru</span></span>
<span data-ttu-id="69abc-121">Верните сервер управления архивацией, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="69abc-121">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="69abc-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69abc-122">-Confirm</span></span>
<span data-ttu-id="69abc-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="69abc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69abc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69abc-124">-WhatIf</span></span>
<span data-ttu-id="69abc-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="69abc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="69abc-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="69abc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69abc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69abc-127">CommonParameters</span></span>
<span data-ttu-id="69abc-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69abc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69abc-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69abc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69abc-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69abc-130">INPUTS</span></span>

### <span data-ttu-id="69abc-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="69abc-131">None</span></span>
<span data-ttu-id="69abc-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="69abc-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69abc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69abc-133">OUTPUTS</span></span>

## <span data-ttu-id="69abc-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="69abc-134">NOTES</span></span>

## <span data-ttu-id="69abc-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69abc-135">RELATED LINKS</span></span>

[<span data-ttu-id="69abc-136">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="69abc-136">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


