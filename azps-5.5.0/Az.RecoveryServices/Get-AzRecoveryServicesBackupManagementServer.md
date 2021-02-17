---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 09d27926f489feea397c98a217840bb973e002ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223396"
---
# <span data-ttu-id="615dc-101">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="615dc-101">Get-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="615dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="615dc-102">SYNOPSIS</span></span>
<span data-ttu-id="615dc-103">Получает серверы управления резервной копией SCDPM и Azure.</span><span class="sxs-lookup"><span data-stu-id="615dc-103">Gets SCDPM and Azure Backup management servers.</span></span>

## <span data-ttu-id="615dc-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="615dc-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupManagementServer [[-Name] <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="615dc-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="615dc-105">DESCRIPTION</span></span>
<span data-ttu-id="615dc-106">Для получения списка серверов управления резервными копиями, зарегистрированных в хранилище, возвращается список серверов **Get-AzRecoveryServicesBackupManagementServer.**</span><span class="sxs-lookup"><span data-stu-id="615dc-106">The **Get-AzRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>
<span data-ttu-id="615dc-107">Существует два типа серверов управления резервным копированием: System Center Data Protection Manager (SCDPM) и серверы управления резервными копиями Azure.</span><span class="sxs-lookup"><span data-stu-id="615dc-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="615dc-108">Серверы управления резервными копиями устанавливаются отдельно для управления архивацией.</span><span class="sxs-lookup"><span data-stu-id="615dc-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>
<span data-ttu-id="615dc-109">Прежде чем использовать текущий Set-AzRecoveryServicesVaultContext, задате контекст хранилища с помощью Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="615dc-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="615dc-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="615dc-110">EXAMPLES</span></span>

### <span data-ttu-id="615dc-111">Пример 1. Получить все серверы управления резервным копированием</span><span class="sxs-lookup"><span data-stu-id="615dc-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupManagementServer
```

<span data-ttu-id="615dc-112">Эта команда получает все серверы управления резервным копированием, зарегистрированные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="615dc-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="615dc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="615dc-113">PARAMETERS</span></span>

### <span data-ttu-id="615dc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="615dc-114">-DefaultProfile</span></span>
<span data-ttu-id="615dc-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="615dc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="615dc-116">-Name</span><span class="sxs-lookup"><span data-stu-id="615dc-116">-Name</span></span>
<span data-ttu-id="615dc-117">Имя сервера управления резервной копией, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="615dc-117">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="615dc-118">-VaultId</span><span class="sxs-lookup"><span data-stu-id="615dc-118">-VaultId</span></span>
<span data-ttu-id="615dc-119">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="615dc-119">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="615dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="615dc-120">CommonParameters</span></span>
<span data-ttu-id="615dc-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="615dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="615dc-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="615dc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="615dc-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="615dc-123">INPUTS</span></span>

### <span data-ttu-id="615dc-124">System.String</span><span class="sxs-lookup"><span data-stu-id="615dc-124">System.String</span></span>

## <span data-ttu-id="615dc-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="615dc-125">OUTPUTS</span></span>

### <span data-ttu-id="615dc-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="615dc-126">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="615dc-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="615dc-127">NOTES</span></span>

## <span data-ttu-id="615dc-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="615dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="615dc-129">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="615dc-129">Unregister-AzRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzRecoveryServicesBackupManagementServer.md)


