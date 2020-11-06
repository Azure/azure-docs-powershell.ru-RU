---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567549"
---
# <span data-ttu-id="26ff3-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="26ff3-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="26ff3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26ff3-102">SYNOPSIS</span></span>
<span data-ttu-id="26ff3-103">Отменяет регистрацию сервера SCDPM или резервного сервера из хранилища.</span><span class="sxs-lookup"><span data-stu-id="26ff3-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26ff3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26ff3-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26ff3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ff3-105">DESCRIPTION</span></span>
<span data-ttu-id="26ff3-106">Командлет **Unregister-AzureRmRecoveryServicesBackupManagementServer** отменяет регистрацию сервера System Center Data Protection Manager (SCDPM) или резервного сервера Azure из хранилища.</span><span class="sxs-lookup"><span data-stu-id="26ff3-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="26ff3-107">Этот командлет удаляет ссылки на серверы, которые не зарегистрированы в хранилище.</span><span class="sxs-lookup"><span data-stu-id="26ff3-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="26ff3-108">Прежде чем можно будет отменить регистрацию контейнера, необходимо удалить все защищенные данные, связанные с этим контейнером.</span><span class="sxs-lookup"><span data-stu-id="26ff3-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="26ff3-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="26ff3-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="26ff3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26ff3-110">EXAMPLES</span></span>

### <span data-ttu-id="26ff3-111">Пример 1: Отмена регистрации сервера SCDPM в хранилище</span><span class="sxs-lookup"><span data-stu-id="26ff3-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="26ff3-112">Первая команда получает сервер управления архивацией с именем dpmserver01.contoso.com и сохраняет его в переменной $BMS.</span><span class="sxs-lookup"><span data-stu-id="26ff3-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="26ff3-113">Вторая команда отменяет регистрацию сервера SCDPM в хранилище.</span><span class="sxs-lookup"><span data-stu-id="26ff3-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="26ff3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26ff3-114">PARAMETERS</span></span>

### <span data-ttu-id="26ff3-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="26ff3-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="26ff3-116">Указывает объект сервера SCDPM, который нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="26ff3-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="26ff3-117">Чтобы получить объект **BackupManagementServer** , используйте командлет Get-AzureRmRecoveryServicesBackupManagementServer.</span><span class="sxs-lookup"><span data-stu-id="26ff3-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="26ff3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26ff3-118">-DefaultProfile</span></span>
<span data-ttu-id="26ff3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26ff3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26ff3-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26ff3-120">CommonParameters</span></span>
<span data-ttu-id="26ff3-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26ff3-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26ff3-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26ff3-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26ff3-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26ff3-123">INPUTS</span></span>

## <span data-ttu-id="26ff3-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26ff3-124">OUTPUTS</span></span>

## <span data-ttu-id="26ff3-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="26ff3-125">NOTES</span></span>

## <span data-ttu-id="26ff3-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26ff3-126">RELATED LINKS</span></span>

[<span data-ttu-id="26ff3-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="26ff3-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


