---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: bd4945436c840323121be7a4450a0042acf67cde
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218004"
---
# <span data-ttu-id="2bd10-101">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2bd10-101">Get-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="2bd10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd10-102">SYNOPSIS</span></span>

<span data-ttu-id="2bd10-103">Получает контейнеры резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2bd10-103">Gets Backup containers.</span></span>

## <span data-ttu-id="2bd10-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2bd10-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-FriendlyName] <String>] [[-ResourceGroupName] <String>] [[-Status] <ContainerRegistrationStatus>]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bd10-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bd10-105">DESCRIPTION</span></span>

<span data-ttu-id="2bd10-106">Для получения контейнера резервной копии возвращается cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="2bd10-106">The **Get-AzRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span> <span data-ttu-id="2bd10-107">Контейнер резервного копирования— это источники данных, моделируются как элементы резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2bd10-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>
<span data-ttu-id="2bd10-108">В выходных данных для контейнеров типа "Azure VM" перечислены все контейнеры, имя которых в точности соответствует одному из переданных в качестве значения параметра Friendly Name.</span><span class="sxs-lookup"><span data-stu-id="2bd10-108">For Container type "Azure VM" , the output lists all the containers whose name exactly matches to the one passed  as the value for Friendly Name parameter.</span></span> <span data-ttu-id="2bd10-109">Для других типов контейнеров выводит список контейнеров с именем, похожим на значение, переданное параметру Friendly name.</span><span class="sxs-lookup"><span data-stu-id="2bd10-109">For other container types,  output gives a list of containers with name similar to the value passed for Friendly name parameter.</span></span>
<span data-ttu-id="2bd10-110">Задать контекст хранилища с помощью параметра -VaultId.</span><span class="sxs-lookup"><span data-stu-id="2bd10-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="2bd10-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2bd10-111">EXAMPLES</span></span>

### <span data-ttu-id="2bd10-112">Пример 1. Получите определенный контейнер</span><span class="sxs-lookup"><span data-stu-id="2bd10-112">Example 1: Get a specific container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType "AzureVM" -Status "Registered" -FriendlyName "V2VM" -VaultId $vault.ID
```

<span data-ttu-id="2bd10-113">Эта команда получает контейнер с именем V2VM типа AzureVM.</span><span class="sxs-lookup"><span data-stu-id="2bd10-113">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="2bd10-114">Пример 2. Получить все контейнеры определенного типа</span><span class="sxs-lookup"><span data-stu-id="2bd10-114">Example 2: Get all containers of a specific type</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Get-AzRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS -VaultId $vault.ID
```

<span data-ttu-id="2bd10-115">Эта команда возвращает все контейнеры Windows, защищенные агентом резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd10-115">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="2bd10-116">Параметр **BackupManagementType** требуется только для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="2bd10-116">The **BackupManagementType** parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="2bd10-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bd10-117">PARAMETERS</span></span>

### <span data-ttu-id="2bd10-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="2bd10-118">-BackupManagementType</span></span>

<span data-ttu-id="2bd10-119">Класс защищенных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bd10-119">The class of resources being protected.</span></span> <span data-ttu-id="2bd10-120">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2bd10-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bd10-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2bd10-121">AzureVM</span></span>
- <span data-ttu-id="2bd10-122">MARS</span><span class="sxs-lookup"><span data-stu-id="2bd10-122">MARS</span></span>
- <span data-ttu-id="2bd10-123">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="2bd10-123">AzureWorkload</span></span>
- <span data-ttu-id="2bd10-124">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="2bd10-124">AzureStorage</span></span>

<span data-ttu-id="2bd10-125">Этот параметр используется для дифференцирования компьютеров Windows, резервных копий с помощью агента MARS или других резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2bd10-125">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

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

### <span data-ttu-id="2bd10-126">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="2bd10-126">-ContainerType</span></span>

<span data-ttu-id="2bd10-127">Тип контейнера резервной копии.</span><span class="sxs-lookup"><span data-stu-id="2bd10-127">Specifies the backup container type.</span></span>
<span data-ttu-id="2bd10-128">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2bd10-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bd10-129">AzureVM</span><span class="sxs-lookup"><span data-stu-id="2bd10-129">AzureVM</span></span>
- <span data-ttu-id="2bd10-130">Windows</span><span class="sxs-lookup"><span data-stu-id="2bd10-130">Windows</span></span>
- <span data-ttu-id="2bd10-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="2bd10-131">AzureStorage</span></span>
- <span data-ttu-id="2bd10-132">AzureVMAppContainer</span><span class="sxs-lookup"><span data-stu-id="2bd10-132">AzureVMAppContainer</span></span>

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

### <span data-ttu-id="2bd10-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd10-133">-DefaultProfile</span></span>

<span data-ttu-id="2bd10-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd10-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd10-135">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="2bd10-135">-FriendlyName</span></span>

<span data-ttu-id="2bd10-136">Указывает удобное имя контейнера, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2bd10-136">Specifies the friendly name of the container to get.</span></span>

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

### <span data-ttu-id="2bd10-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bd10-137">-ResourceGroupName</span></span>

<span data-ttu-id="2bd10-138">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bd10-138">Specifies the name of the resource group.</span></span>
<span data-ttu-id="2bd10-139">Этот параметр используется только для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd10-139">This parameter is for Azure virtual machines only.</span></span>

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

### <span data-ttu-id="2bd10-140">-Status</span><span class="sxs-lookup"><span data-stu-id="2bd10-140">-Status</span></span>

<span data-ttu-id="2bd10-141">Указывает состояние регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="2bd10-141">Specifies the container registration status.</span></span>
<span data-ttu-id="2bd10-142">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2bd10-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2bd10-143">Зарегистрированы</span><span class="sxs-lookup"><span data-stu-id="2bd10-143">Registered</span></span>

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

### <span data-ttu-id="2bd10-144">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2bd10-144">-VaultId</span></span>

<span data-ttu-id="2bd10-145">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="2bd10-145">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2bd10-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd10-146">CommonParameters</span></span>
<span data-ttu-id="2bd10-147">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd10-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd10-148">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bd10-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd10-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bd10-149">INPUTS</span></span>

### <span data-ttu-id="2bd10-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2bd10-150">System.String</span></span>

## <span data-ttu-id="2bd10-151">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bd10-151">OUTPUTS</span></span>

### <span data-ttu-id="2bd10-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="2bd10-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="2bd10-153">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2bd10-153">NOTES</span></span>

## <span data-ttu-id="2bd10-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bd10-154">RELATED LINKS</span></span>

[<span data-ttu-id="2bd10-155">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="2bd10-155">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="2bd10-156">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="2bd10-156">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="2bd10-157">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="2bd10-157">Unregister-AzRecoveryServicesBackupContainer</span></span>](./Unregister-AzRecoveryServicesBackupContainer.md)
