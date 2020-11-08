---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: f061dc0f729709dee3bfe08bb22dba8d49a7f31b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077695"
---
# <span data-ttu-id="9f0b4-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9f0b4-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="9f0b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f0b4-102">SYNOPSIS</span></span>

<span data-ttu-id="9f0b4-103">Получает контейнеры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-103">Gets Backup containers.</span></span>

## <span data-ttu-id="9f0b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f0b4-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f0b4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f0b4-105">DESCRIPTION</span></span>

<span data-ttu-id="9f0b4-106">Командлет **Get-AzRecoveryServicesBackupContainer** получает контейнер резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="9f0b4-107">Контейнер резервного копирования инкапсулирует источники данных, которые моделируются как элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="9f0b4-108">Задайте контекст хранилища с помощью параметра-VaultId.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="9f0b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f0b4-109">EXAMPLES</span></span>

### <span data-ttu-id="9f0b4-110">Пример 1: получение определенного контейнера</span><span class="sxs-lookup"><span data-stu-id="9f0b4-110">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="9f0b4-111">Эта команда получает контейнер с именем V2VM типа AzureVM.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="9f0b4-112">Пример 2: получение всех контейнеров определенного типа</span><span class="sxs-lookup"><span data-stu-id="9f0b4-112">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="9f0b4-113">Эта команда получает все контейнеры окон, защищенные агентом резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="9f0b4-114">Параметр **BackupManagementType** требуется только для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-114">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="9f0b4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f0b4-115">PARAMETERS</span></span>

### <span data-ttu-id="9f0b4-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="9f0b4-116">-BackupManagementType</span></span>

<span data-ttu-id="9f0b4-117">Класс защищаемых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-117">The class of resources being protected.</span></span> <span data-ttu-id="9f0b4-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f0b4-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9f0b4-119">AzureVM</span></span>
- <span data-ttu-id="9f0b4-120">Марс</span><span class="sxs-lookup"><span data-stu-id="9f0b4-120">MARS</span></span>
- <span data-ttu-id="9f0b4-121">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="9f0b4-121">AzureWorkload</span></span>
- <span data-ttu-id="9f0b4-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="9f0b4-122">AzureStorage</span></span>

<span data-ttu-id="9f0b4-123">Этот параметр используется для различения компьютеров с Windows, которые были заархивированы с помощью агента MARS или других резервных модулей.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="9f0b4-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="9f0b4-124">-ContainerType</span></span>

<span data-ttu-id="9f0b4-125">Указывает тип контейнера резервной копии.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-125">Specifies the backup container type.</span></span>
<span data-ttu-id="9f0b4-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f0b4-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="9f0b4-127">AzureVM</span></span>
- <span data-ttu-id="9f0b4-128">Windows</span><span class="sxs-lookup"><span data-stu-id="9f0b4-128">Windows</span></span>
- <span data-ttu-id="9f0b4-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="9f0b4-129">AzureSQL</span></span>
- <span data-ttu-id="9f0b4-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="9f0b4-130">AzureStorage</span></span>
- <span data-ttu-id="9f0b4-131">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="9f0b4-131">AzureVMAppContainer</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureVMAppContainer

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f0b4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0b4-132">-DefaultProfile</span></span>

<span data-ttu-id="9f0b4-133">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f0b4-134">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="9f0b4-134">-FriendlyName</span></span>

<span data-ttu-id="9f0b4-135">Указывает понятное имя контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-135">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="9f0b4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f0b4-136">-ResourceGroupName</span></span>

<span data-ttu-id="9f0b4-137">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-137">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9f0b4-138">Этот параметр предназначен только для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-138">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="9f0b4-139">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="9f0b4-139">-Status</span></span>

<span data-ttu-id="9f0b4-140">Указывает состояние регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-140">Specifies the container registration status.</span></span>
<span data-ttu-id="9f0b4-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="9f0b4-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9f0b4-142">Пользователь</span><span class="sxs-lookup"><span data-stu-id="9f0b4-142">Registered</span></span>

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

### <span data-ttu-id="9f0b4-143">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9f0b4-143">-VaultId</span></span>

<span data-ttu-id="9f0b4-144">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-144">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9f0b4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0b4-145">CommonParameters</span></span>
<span data-ttu-id="9f0b4-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f0b4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0b4-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f0b4-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0b4-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f0b4-148">INPUTS</span></span>

### <span data-ttu-id="9f0b4-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9f0b4-149">System.String</span></span>

## <span data-ttu-id="9f0b4-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f0b4-150">OUTPUTS</span></span>

### <span data-ttu-id="9f0b4-151">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="9f0b4-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="9f0b4-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f0b4-152">NOTES</span></span>

## <span data-ttu-id="9f0b4-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f0b4-153">RELATED LINKS</span></span>

[<span data-ttu-id="9f0b4-154">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="9f0b4-154">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="9f0b4-155">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="9f0b4-155">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="9f0b4-156">Отмена регистрации — AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="9f0b4-156">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)