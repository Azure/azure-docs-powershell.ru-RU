---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 4B7ACEC8-29BB-4791-8087-801300F246B4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: c76bd152f64b337ca818c9e86b14fddbdaaf38cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568711"
---
# <span data-ttu-id="517e1-101">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="517e1-101">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="517e1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="517e1-102">SYNOPSIS</span></span>
<span data-ttu-id="517e1-103">Получает серверы управления архивацией SCDPM и Azure.</span><span class="sxs-lookup"><span data-stu-id="517e1-103">Gets SCDPM and Azure Backup management servers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="517e1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="517e1-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupManagementServer [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="517e1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="517e1-105">DESCRIPTION</span></span>
<span data-ttu-id="517e1-106">Командлет **Get-AzureRmRecoveryServicesBackupManagementServer** получает список серверов управления резервных копий, зарегистрированных в хранилище.</span><span class="sxs-lookup"><span data-stu-id="517e1-106">The **Get-AzureRmRecoveryServicesBackupManagementServer** cmdlet gets a list of Backup management servers that are registered in a vault.</span></span>

<span data-ttu-id="517e1-107">Существует два типа серверов управления резервным копированием: System Center Data Protection Manager (SCDPM) и Azure Backup Management Servers.</span><span class="sxs-lookup"><span data-stu-id="517e1-107">There are two types of Backup management servers: System Center Data Protection Manager (SCDPM) and Azure Backup management servers.</span></span>
<span data-ttu-id="517e1-108">Серверы управления архивацией устанавливаются отдельно для управления управлением резервных копий.</span><span class="sxs-lookup"><span data-stu-id="517e1-108">Backup management servers are installed separately to manage Backup orchestration.</span></span>

<span data-ttu-id="517e1-109">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="517e1-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="517e1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="517e1-110">EXAMPLES</span></span>

### <span data-ttu-id="517e1-111">Пример 1: получение всех серверов управления резервными копиями</span><span class="sxs-lookup"><span data-stu-id="517e1-111">Example 1: Get all Backup management servers</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupManagementServer
```

<span data-ttu-id="517e1-112">Эта команда получает все серверы управления резервными копиями, зарегистрированные в хранилище.</span><span class="sxs-lookup"><span data-stu-id="517e1-112">This command gets all Backup management servers registered with the vault.</span></span>

## <span data-ttu-id="517e1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="517e1-113">PARAMETERS</span></span>

### <span data-ttu-id="517e1-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="517e1-114">-Name</span></span>
<span data-ttu-id="517e1-115">Указывает имя сервера управления резервными копиями, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="517e1-115">Specifies the name of the Backup management server to get.</span></span>

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

### <span data-ttu-id="517e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="517e1-116">-DefaultProfile</span></span>
<span data-ttu-id="517e1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="517e1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="517e1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="517e1-118">CommonParameters</span></span>
<span data-ttu-id="517e1-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="517e1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="517e1-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="517e1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="517e1-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="517e1-121">INPUTS</span></span>

## <span data-ttu-id="517e1-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="517e1-122">OUTPUTS</span></span>

### <span data-ttu-id="517e1-123">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="517e1-123">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

### <span data-ttu-id="517e1-124">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. BackupEngineBase]</span><span class="sxs-lookup"><span data-stu-id="517e1-124">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase]</span></span>

## <span data-ttu-id="517e1-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="517e1-125">NOTES</span></span>

## <span data-ttu-id="517e1-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="517e1-126">RELATED LINKS</span></span>

[<span data-ttu-id="517e1-127">Отмена регистрации — AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="517e1-127">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Unregister-AzureRmRecoveryServicesBackupManagementServer.md)


