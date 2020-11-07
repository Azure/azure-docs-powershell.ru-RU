---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/initialize-azrecoveryservicesbackupprotectableitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Initialize-AzRecoveryServicesBackupProtectableItem.md
ms.openlocfilehash: 0fd0473cccdf8fbef3d3bab941ab6b3ce7813a63
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729677"
---
# <span data-ttu-id="d0dcf-101">Initialize-AzRecoveryServicesBackupProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d0dcf-101">Initialize-AzRecoveryServicesBackupProtectableItem</span></span>

## <span data-ttu-id="d0dcf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d0dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="d0dcf-103">Эта команда запускает обнаружение незащищенных элементов заданного типа рабочей нагрузки в заданном контейнере.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-103">This command triggers the discovery of any unprotected items of the given workload type in the given container.</span></span> <span data-ttu-id="d0dcf-104">Если приложение DB не защищено автоматически, используйте эту команду, чтобы найти новый DBs, когда они будут добавлены, и продолжите их защиту.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-104">If the DB application is not auto-protected use this command to discover new DBs whenever they are added and proceed to protect them.</span></span>

## <span data-ttu-id="d0dcf-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d0dcf-105">SYNTAX</span></span>

```
Initialize-AzRecoveryServicesBackupProtectableItem [-Container] <ContainerBase> [-WorkloadType] <WorkloadType>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0dcf-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0dcf-106">DESCRIPTION</span></span>
<span data-ttu-id="d0dcf-107">Командлет зазапрос для определенных рабочих нагрузок в контейнере.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-107">the cmdlet enquires for specific workloads within a container.</span></span> <span data-ttu-id="d0dcf-108">Это вызывает операцию, которая создает защищенные элементы.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-108">This triggers an operation which creates protectable items.</span></span>

## <span data-ttu-id="d0dcf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d0dcf-109">EXAMPLES</span></span>

### <span data-ttu-id="d0dcf-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d0dcf-110">Example 1</span></span>
```
PS C:\> Initialize-AzRecoveryServicesProtectableItem -Container $Container –WorkloadType “MSSQL”
```

<span data-ttu-id="d0dcf-111">Командлет выполняет операцию обнаружения для новых защищенных элементов.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-111">The cmdlet executes a discovery operation for new protectable items.</span></span>

## <span data-ttu-id="d0dcf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d0dcf-112">PARAMETERS</span></span>

### <span data-ttu-id="d0dcf-113">-Container</span><span class="sxs-lookup"><span data-stu-id="d0dcf-113">-Container</span></span>
<span data-ttu-id="d0dcf-114">Контейнер, в котором находится элемент</span><span class="sxs-lookup"><span data-stu-id="d0dcf-114">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d0dcf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0dcf-115">-DefaultProfile</span></span>
<span data-ttu-id="d0dcf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0dcf-117">-VaultId</span><span class="sxs-lookup"><span data-stu-id="d0dcf-117">-VaultId</span></span>
<span data-ttu-id="d0dcf-118">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-118">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="d0dcf-119">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="d0dcf-119">-WorkloadType</span></span>
<span data-ttu-id="d0dcf-120">Тип рабочей нагрузки ресурса (например,: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="d0dcf-120">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0dcf-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0dcf-121">CommonParameters</span></span>
<span data-ttu-id="d0dcf-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d0dcf-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0dcf-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0dcf-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0dcf-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d0dcf-124">INPUTS</span></span>

### <span data-ttu-id="d0dcf-125">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="d0dcf-125">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>
<span data-ttu-id="d0dcf-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d0dcf-126">System.String</span></span>

## <span data-ttu-id="d0dcf-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d0dcf-127">OUTPUTS</span></span>

### <span data-ttu-id="d0dcf-128">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="d0dcf-128">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="d0dcf-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d0dcf-129">NOTES</span></span>

## <span data-ttu-id="d0dcf-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d0dcf-130">RELATED LINKS</span></span>