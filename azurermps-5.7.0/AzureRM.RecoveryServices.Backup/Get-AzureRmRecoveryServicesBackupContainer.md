---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 1097FF29-1C23-4960-930C-5C1227419359
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupContainer.md
ms.openlocfilehash: c861c9f18f2fb91838b8e527e2c3ee637098c00a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558955"
---
# <span data-ttu-id="b425a-101">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b425a-101">Get-AzureRmRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="b425a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b425a-102">SYNOPSIS</span></span>
<span data-ttu-id="b425a-103">Получает контейнеры резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b425a-103">Gets Backup containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b425a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b425a-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupContainer [-ContainerType] <ContainerType> [[-BackupManagementType] <String>]
 [[-Name] <String>] [[-FriendlyName] <String>] [[-ResourceGroupName] <String>]
 [[-Status] <ContainerRegistrationStatus>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b425a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b425a-105">DESCRIPTION</span></span>
<span data-ttu-id="b425a-106">Командлет **Get-AzureRmRecoveryServicesBackupContainer** получает контейнер резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b425a-106">The **Get-AzureRmRecoveryServicesBackupContainer** cmdlet gets a backup container.</span></span>
<span data-ttu-id="b425a-107">Контейнер резервного копирования инкапсулирует источники данных, которые моделируются как элементы резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="b425a-107">A Backup container encapsulates data sources that are modelled as backup items.</span></span>

<span data-ttu-id="b425a-108">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="b425a-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b425a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b425a-109">EXAMPLES</span></span>

### <span data-ttu-id="b425a-110">Пример 1: получение определенного контейнера</span><span class="sxs-lookup"><span data-stu-id="b425a-110">Example 1: Get a specific container</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesContainer -ContainerType "AzureVM" -Status "Registered" -Name "V2VM";
```

<span data-ttu-id="b425a-111">Эта команда получает контейнер с именем V2VM типа AzureVM.</span><span class="sxs-lookup"><span data-stu-id="b425a-111">This command gets the container named V2VM of type AzureVM.</span></span>

### <span data-ttu-id="b425a-112">Пример 2: получение всех контейнеров определенного типа</span><span class="sxs-lookup"><span data-stu-id="b425a-112">Example 2: Get all containers of a specific type</span></span>
```
PS C:\>Get-AzureRmRecoveryServicesBackupContainer -ContainerType Windows -BackupManagementType MARS
```

<span data-ttu-id="b425a-113">Эта команда получает все контейнеры окон, защищенные агентом резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="b425a-113">This command gets all Windows containers that are protected by Azure Backup agent.</span></span>
<span data-ttu-id="b425a-114">Параметр *BackupManagementType* требуется только для контейнеров Windows.</span><span class="sxs-lookup"><span data-stu-id="b425a-114">The *BackupManagementType* parameter is only required for Windows containers.</span></span>

## <span data-ttu-id="b425a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b425a-115">PARAMETERS</span></span>

### <span data-ttu-id="b425a-116">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b425a-116">-BackupManagementType</span></span>
<span data-ttu-id="b425a-117">Указывает тип управления резервным копированием.</span><span class="sxs-lookup"><span data-stu-id="b425a-117">Specifies the backup management type.</span></span>
<span data-ttu-id="b425a-118">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b425a-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b425a-119">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b425a-119">AzureVM</span></span>
- <span data-ttu-id="b425a-120">Марс</span><span class="sxs-lookup"><span data-stu-id="b425a-120">MARS</span></span>
- <span data-ttu-id="b425a-121">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="b425a-121">AzureSQL</span></span>

<span data-ttu-id="b425a-122">Этот параметр используется для различения компьютеров с Windows, которые были заархивированы с помощью агента MARS или других резервных модулей.</span><span class="sxs-lookup"><span data-stu-id="b425a-122">This parameter is used to differentiate Windows machines that are backed up using MARS agent or other backup engines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, MARS, AzureSQL

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-123">-ContainerType</span><span class="sxs-lookup"><span data-stu-id="b425a-123">-ContainerType</span></span>
<span data-ttu-id="b425a-124">Указывает тип контейнера резервной копии.</span><span class="sxs-lookup"><span data-stu-id="b425a-124">Specifies the backup container type.</span></span>
<span data-ttu-id="b425a-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b425a-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b425a-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b425a-126">AzureVM</span></span> 
- <span data-ttu-id="b425a-127">Windows</span><span class="sxs-lookup"><span data-stu-id="b425a-127">Windows</span></span>
- <span data-ttu-id="b425a-128">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="b425a-128">AzureSQL</span></span>

```yaml
Type: ContainerType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, Windows, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b425a-129">-DefaultProfile</span></span>
<span data-ttu-id="b425a-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b425a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b425a-131">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b425a-131">-FriendlyName</span></span>
<span data-ttu-id="b425a-132">Указывает понятное имя контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b425a-132">Specifies the friendly name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b425a-133">-Name</span></span>
<span data-ttu-id="b425a-134">Указывает имя контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="b425a-134">Specifies the name of the container to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b425a-135">-ResourceGroupName</span></span>
<span data-ttu-id="b425a-136">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b425a-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b425a-137">Этот параметр предназначен только для виртуальных машин Azure.</span><span class="sxs-lookup"><span data-stu-id="b425a-137">This parameter is for Azure virtual machines only.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-138">-Status (состояние)</span><span class="sxs-lookup"><span data-stu-id="b425a-138">-Status</span></span>
<span data-ttu-id="b425a-139">Указывает состояние регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="b425a-139">Specifies the container registration status.</span></span>
<span data-ttu-id="b425a-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b425a-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b425a-141">Пользователь</span><span class="sxs-lookup"><span data-stu-id="b425a-141">Registered</span></span>

```yaml
Type: ContainerRegistrationStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Registered

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b425a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b425a-142">CommonParameters</span></span>
<span data-ttu-id="b425a-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b425a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b425a-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b425a-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b425a-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b425a-145">INPUTS</span></span>

### <span data-ttu-id="b425a-146">Ничего</span><span class="sxs-lookup"><span data-stu-id="b425a-146">None</span></span>
<span data-ttu-id="b425a-147">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="b425a-147">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b425a-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b425a-148">OUTPUTS</span></span>

### <span data-ttu-id="b425a-149">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b425a-149">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="b425a-150">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ContainerBase]</span><span class="sxs-lookup"><span data-stu-id="b425a-150">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase]</span></span>

## <span data-ttu-id="b425a-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="b425a-151">NOTES</span></span>

## <span data-ttu-id="b425a-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b425a-152">RELATED LINKS</span></span>

[<span data-ttu-id="b425a-153">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b425a-153">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="b425a-154">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b425a-154">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)

[<span data-ttu-id="b425a-155">Отмена регистрации — AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="b425a-155">Unregister-AzureRmRecoveryServicesBackupContainer</span></span>](./Unregister-AzureRmRecoveryServicesBackupContainer.md)


