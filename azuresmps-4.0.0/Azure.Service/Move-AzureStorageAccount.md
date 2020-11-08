---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076239"
---
# <span data-ttu-id="b4b44-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b4b44-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="b4b44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b4b44-102">SYNOPSIS</span></span>
<span data-ttu-id="b4b44-103">Миграция учетной записи хранения в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b44-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4b44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b4b44-104">SYNTAX</span></span>

### <span data-ttu-id="b4b44-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b44-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4b44-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b44-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4b44-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b44-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b4b44-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4b44-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b4b44-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b44-109">DESCRIPTION</span></span>
<span data-ttu-id="b4b44-110">Командлет **Move-AzureStorageAccount** выполняет миграцию учетной записи хранения в группу ресурсов в стеке диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b44-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4b44-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b4b44-111">EXAMPLES</span></span>

### <span data-ttu-id="b4b44-112">Пример 1: подготовка миграции учетной записи хранилища</span><span class="sxs-lookup"><span data-stu-id="b4b44-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="b4b44-113">Эта команда подготавливает учетную запись хранения с именем ContosoStorageName для миграции в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b44-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b4b44-114">Пример 2: Запуск миграции учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b4b44-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="b4b44-115">Эта команда запускает миграцию учетной записи хранения с именем ContosoStorageName в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b44-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="b4b44-116">Пример 3: Проверка миграции учетных записей хранения</span><span class="sxs-lookup"><span data-stu-id="b4b44-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="b4b44-117">Эта команда проверяет миграцию учетной записи хранения с именем ContosoStorageName в стек диспетчера ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="b4b44-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="b4b44-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b4b44-118">PARAMETERS</span></span>

### <span data-ttu-id="b4b44-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="b4b44-119">-Abort</span></span>
<span data-ttu-id="b4b44-120">Указывает, что этот командлет отменяет миграцию учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b4b44-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="b4b44-121">-Commit</span></span>
<span data-ttu-id="b4b44-122">Указывает на то, что этот командлет запускает миграцию учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b4b44-122">Indicates that this cmdlet starts the storage account migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b4b44-123">-InformationAction</span></span>
<span data-ttu-id="b4b44-124">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="b4b44-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b4b44-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="b4b44-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b4b44-126">Продолжал</span><span class="sxs-lookup"><span data-stu-id="b4b44-126">Continue</span></span>
- <span data-ttu-id="b4b44-127">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="b4b44-127">Ignore</span></span>
- <span data-ttu-id="b4b44-128">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="b4b44-128">Inquire</span></span>
- <span data-ttu-id="b4b44-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b4b44-129">SilentlyContinue</span></span>
- <span data-ttu-id="b4b44-130">Остановить</span><span class="sxs-lookup"><span data-stu-id="b4b44-130">Stop</span></span>
- <span data-ttu-id="b4b44-131">Рвать</span><span class="sxs-lookup"><span data-stu-id="b4b44-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b4b44-132">-InformationVariable</span></span>
<span data-ttu-id="b4b44-133">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="b4b44-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-134">-Подготовка</span><span class="sxs-lookup"><span data-stu-id="b4b44-134">-Prepare</span></span>
<span data-ttu-id="b4b44-135">Указывает на то, что этот командлет подготавливает учетную запись хранения для миграции.</span><span class="sxs-lookup"><span data-stu-id="b4b44-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="b4b44-136">-Profile</span></span>
<span data-ttu-id="b4b44-137">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b4b44-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b4b44-138">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b4b44-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4b44-139">-StorageAccountName</span></span>
<span data-ttu-id="b4b44-140">Указывает имя учетной записи хранения, которая переносится этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="b4b44-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-141">-Проверка</span><span class="sxs-lookup"><span data-stu-id="b4b44-141">-Validate</span></span>
<span data-ttu-id="b4b44-142">Указывает, что этот командлет проверяет учетную запись хранения для миграции.</span><span class="sxs-lookup"><span data-stu-id="b4b44-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4b44-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4b44-143">CommonParameters</span></span>
<span data-ttu-id="b4b44-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b4b44-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4b44-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4b44-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4b44-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b4b44-146">INPUTS</span></span>

## <span data-ttu-id="b4b44-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b4b44-147">OUTPUTS</span></span>

## <span data-ttu-id="b4b44-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="b4b44-148">NOTES</span></span>

## <span data-ttu-id="b4b44-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b4b44-149">RELATED LINKS</span></span>

[<span data-ttu-id="b4b44-150">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="b4b44-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="b4b44-151">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="b4b44-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="b4b44-152">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="b4b44-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="b4b44-153">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="b4b44-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="b4b44-154">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b4b44-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


