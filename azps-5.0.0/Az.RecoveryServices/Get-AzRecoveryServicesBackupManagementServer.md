---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245710"
---
# <span data-ttu-id="14de7-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="14de7-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="14de7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14de7-102">SYNOPSIS</span></span>
<span data-ttu-id="14de7-103">Получает серверы управления архивацией SCDPM и Azure.</span><span class="sxs-lookup"><span data-stu-id="14de7-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="14de7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14de7-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14de7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14de7-105">DESCRIPTION</span></span>
<span data-ttu-id="14de7-106">Командлет **Get-AzRecoveryServicesBackupManagementServer** получает список серверов управления резервных копий, зарегистрированных в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14de7-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="14de7-107">Существует два типа серверов управления резервным копированием: System Center Data Protection Manager (SCDPM) и Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="14de7-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="14de7-108">Серверы управления архивацией устанавливаются отдельно для управления управлением резервных копий.</span><span class="sxs-lookup"><span data-stu-id="14de7-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="14de7-109">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="14de7-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="14de7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14de7-110">EXAMPLES</span></span>

### <span data-ttu-id="14de7-111">Пример 1: получение всех серверов управления резервными копиями</span><span class="sxs-lookup"><span data-stu-id="14de7-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="14de7-112">Эта команда получает все серверы управления резервными копиями, зарегистрированные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="14de7-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="14de7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14de7-113">PARAMETERS</span></span>

### <span data-ttu-id="14de7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14de7-114">-DefaultProfile</span></span>
<span data-ttu-id="14de7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="14de7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14de7-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="14de7-116">-Name</span></span>
<span data-ttu-id="14de7-117">Указывает имя сервера управления резервными копиями, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="14de7-117">Specifies the name of the Backup management server to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14de7-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="14de7-118">-VaultId</span></span>
<span data-ttu-id="14de7-119">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="14de7-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="14de7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14de7-120">CommonParameters</span></span>
<span data-ttu-id="14de7-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14de7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14de7-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14de7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14de7-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14de7-123">INPUTS</span></span>

### <span data-ttu-id="14de7-124">System. String</span><span class="sxs-lookup"><span data-stu-id="14de7-124">System.String</span></span>

## <span data-ttu-id="14de7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14de7-125">OUTPUTS</span></span>

### <span data-ttu-id="14de7-126">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="14de7-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="14de7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="14de7-127">NOTES</span></span>

## <span data-ttu-id="14de7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14de7-128">RELATED LINKS</span></span>

[<span data-ttu-id="14de7-129">Отмена регистрации — AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="14de7-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)

