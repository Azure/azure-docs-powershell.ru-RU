---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 90532c6d314c78e6b7242ec480b95991138719de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508097"
---
# <span data-ttu-id="15a37-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="15a37-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="15a37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a37-102">SYNOPSIS</span></span>

<span data-ttu-id="15a37-103">Получает контейнеры резервных копий.</span><span class="sxs-lookup"><span data-stu-id="15a37-103">Gets Backup containers.</span></span>

## <span data-ttu-id="15a37-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="15a37-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15a37-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15a37-105">DESCRIPTION</span></span>

<span data-ttu-id="15a37-106">Для получения контейнера резервной копии возвращается cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="15a37-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="15a37-107">Контейнер резервного копирования инкапсулирует источники данных, которые моделируются как элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="15a37-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="15a37-108">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="15a37-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="15a37-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="15a37-109">EXAMPLES</span></span>

### <span data-ttu-id="15a37-110">Пример 1. Получите определенный контейнер</span><span class="sxs-lookup"><span data-stu-id="15a37-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="15a37-111">Эта команда получает контейнер с именем V2VM типа AzureVM.</span><span class="sxs-lookup"><span data-stu-id="15a37-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="15a37-112">Пример 2. Получить все контейнеры определенного типа</span><span class="sxs-lookup"><span data-stu-id="15a37-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="15a37-113">Эта команда возвращает все контейнеры Windows, защищенные агентом резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="15a37-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="15a37-114">Параметр **BackupManagementType** требуется только для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="15a37-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="15a37-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15a37-115">PARAMETERS</span></span>

### <span data-ttu-id="15a37-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="15a37-116">-BackupManagementType</span></span>

<span data-ttu-id="15a37-117">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15a37-117">The class of resources being protected.</span></span> <span data-ttu-id="15a37-118">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="15a37-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15a37-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="15a37-119">AzureVM</span></span>
- <span data-ttu-id="15a37-120">MARS</span><span class="sxs-lookup"><span data-stu-id="15a37-120">MARS</span></span>
- <span data-ttu-id="15a37-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="15a37-121">AzureWorkload</span></span>
- <span data-ttu-id="15a37-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="15a37-122">AzureStorage</span></span>

<span data-ttu-id="15a37-123">Этот параметр используется для дифференцирования компьютеров Windows, резервных копий с помощью агента MARS или других резервных копий.</span><span class="sxs-lookup"><span data-stu-id="15a37-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureWorkload, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a37-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="15a37-124">-ContainerType</span></span>

<span data-ttu-id="15a37-125">Тип контейнера резервной копии.</span><span class="sxs-lookup"><span data-stu-id="15a37-125">Specifies the backup container type.</span></span>
<span data-ttu-id="15a37-126">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="15a37-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15a37-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="15a37-127">AzureVM</span></span>
- <span data-ttu-id="15a37-128">Windows</span><span class="sxs-lookup"><span data-stu-id="15a37-128">Windows</span></span>
- <span data-ttu-id="15a37-129">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="15a37-129">AzureStorage</span></span>
- <span data-ttu-id="15a37-130">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="15a37-130">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a37-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a37-131">-DefaultProfile</span></span>

<span data-ttu-id="15a37-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15a37-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a37-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="15a37-133">-FriendlyName</span></span>

<span data-ttu-id="15a37-134">Указывает удобное имя контейнера, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="15a37-134">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a37-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a37-135">-ResourceGroupName</span></span>

<span data-ttu-id="15a37-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="15a37-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="15a37-137">Этот параметр используется только для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="15a37-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a37-138">-Status</span><span class="sxs-lookup"><span data-stu-id="15a37-138">-Status</span></span>

<span data-ttu-id="15a37-139">Указывает состояние регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="15a37-139">Specifies the container registration status.</span></span>
<span data-ttu-id="15a37-140">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="15a37-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15a37-141">Зарегистрированы</span><span class="sxs-lookup"><span data-stu-id="15a37-141">Registered</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerRegistrationStatus
Parameter Sets: (All)
Aliases:
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a37-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="15a37-142">-VaultId</span></span>

<span data-ttu-id="15a37-143">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="15a37-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="15a37-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a37-144">CommonParameters</span></span>
<span data-ttu-id="15a37-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a37-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a37-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15a37-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a37-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="15a37-147">INPUTS</span></span>

### <span data-ttu-id="15a37-148">System.String</span><span class="sxs-lookup"><span data-stu-id="15a37-148">System.String</span></span>

## <span data-ttu-id="15a37-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="15a37-149">OUTPUTS</span></span>

### <span data-ttu-id="15a37-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="15a37-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="15a37-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="15a37-151">NOTES</span></span>

## <span data-ttu-id="15a37-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15a37-152">RELATED LINKS</span></span>

[<span data-ttu-id="15a37-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="15a37-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="15a37-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="15a37-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="15a37-155">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="15a37-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
