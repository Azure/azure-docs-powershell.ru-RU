---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 73438a3f294aaece7c4649f53559311d95ef4aa0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729714"
---
# <span data-ttu-id="37729-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="37729-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="37729-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="37729-102">SYNOPSIS</span></span>
<span data-ttu-id="37729-103">Получает контейнеры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="37729-103">Gets Backup containers.</span></span>

## <span data-ttu-id="37729-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="37729-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37729-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="37729-105">DESCRIPTION</span></span>
<span data-ttu-id="37729-106">Командлет **Get-AzRecoveryServicesBackupContainer** получает контейнер резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="37729-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="37729-107">Контейнер резервного копирования инкапсулирует источники данных, которые моделируются как элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="37729-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="37729-108">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="37729-108">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="37729-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="37729-109">EXAMPLES</span></span>

### <span data-ttu-id="37729-110">Пример 1: получение определенного контейнера</span><span class="sxs-lookup"><span data-stu-id="37729-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="37729-111">Эта команда получает контейнер с именем V2VM типа AzureVM.</span><span class="sxs-lookup"><span data-stu-id="37729-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="37729-112">Пример 2: получение всех контейнеров определенного типа</span><span class="sxs-lookup"><span data-stu-id="37729-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="37729-113">Эта команда получает все контейнеры окон, защищенные агентом резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="37729-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="37729-114">Параметр *BackupManagementType* требуется только для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="37729-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="37729-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="37729-115">PARAMETERS</span></span>

### <span data-ttu-id="37729-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="37729-116">-BackupManagementType</span></span>
<span data-ttu-id="37729-117">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="37729-117">Specifies the backup management type.</span></span>
<span data-ttu-id="37729-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37729-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37729-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="37729-119">AzureVM</span></span>
- <span data-ttu-id="37729-120">Марс</span><span class="sxs-lookup"><span data-stu-id="37729-120">MARS</span></span>
- <span data-ttu-id="37729-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="37729-121">AzureSQL</span></span>
- <span data-ttu-id="37729-122">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="37729-122">AzureStorage</span></span>

<span data-ttu-id="37729-123">Этот параметр используется для различения компьютеров с Windows, которые были заархивированы с помощью агента MARS или других резервных модулей.</span><span class="sxs-lookup"><span data-stu-id="37729-123">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, AzureSQL, AzureStorage

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37729-124">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="37729-124">-ContainerType</span></span>
<span data-ttu-id="37729-125">Указывает тип контейнера резервной копии.</span><span class="sxs-lookup"><span data-stu-id="37729-125">Specifies the backup container type.</span></span>
<span data-ttu-id="37729-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37729-126">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37729-127">AzureVM</span><span class="sxs-lookup"><span data-stu-id="37729-127">AzureVM</span></span> 
- <span data-ttu-id="37729-128">Windows</span><span class="sxs-lookup"><span data-stu-id="37729-128">Windows</span></span>
- <span data-ttu-id="37729-129">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="37729-129">AzureSQL</span></span>
- <span data-ttu-id="37729-130">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="37729-130">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, Windows, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37729-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37729-131">-DefaultProfile</span></span>
<span data-ttu-id="37729-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="37729-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37729-133">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="37729-133">-FriendlyName</span></span>
<span data-ttu-id="37729-134">Указывает понятное имя контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="37729-134">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="37729-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37729-135">-ResourceGroupName</span></span>
<span data-ttu-id="37729-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="37729-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="37729-137">Этот параметр предназначен только для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="37729-137">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="37729-138">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="37729-138">-Status</span></span>
<span data-ttu-id="37729-139">Указывает состояние регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="37729-139">Specifies the container registration status.</span></span>
<span data-ttu-id="37729-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="37729-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="37729-141">Пользователь</span><span class="sxs-lookup"><span data-stu-id="37729-141">Registered</span></span>

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

### <span data-ttu-id="37729-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="37729-142">-VaultId</span></span>
<span data-ttu-id="37729-143">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="37729-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="37729-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37729-144">CommonParameters</span></span>
<span data-ttu-id="37729-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="37729-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37729-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37729-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37729-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="37729-147">INPUTS</span></span>

### <span data-ttu-id="37729-148">System. String</span><span class="sxs-lookup"><span data-stu-id="37729-148">System.String</span></span>

## <span data-ttu-id="37729-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="37729-149">OUTPUTS</span></span>

### <span data-ttu-id="37729-150">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="37729-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="37729-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="37729-151">NOTES</span></span>

## <span data-ttu-id="37729-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="37729-152">RELATED LINKS</span></span>

[<span data-ttu-id="37729-153">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="37729-153">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="37729-154">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="37729-154">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="37729-155">Отмена регистрации — AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="37729-155">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)

