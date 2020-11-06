---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 95FF3F7A-5CC6-4AA6-A393-5EBB5579D9A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupVault.md
ms.openlocfilehash: ef4d8ca2e1fb21165281375b3d325f5fc8b6ceed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560519"
---
# <span data-ttu-id="18441-101">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18441-101">Get-AzureRmBackupVault</span></span>

## <span data-ttu-id="18441-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="18441-102">SYNOPSIS</span></span>
<span data-ttu-id="18441-103">Возвращает хранилище резервных копий.</span><span class="sxs-lookup"><span data-stu-id="18441-103">Gets Backup vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18441-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="18441-104">SYNTAX</span></span>

```
Get-AzureRmBackupVault [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18441-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="18441-105">DESCRIPTION</span></span>
<span data-ttu-id="18441-106">Командлет **Get-AzureRmBackupVault** получает резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="18441-106">The **Get-AzureRmBackupVault** cmdlet gets Azure Backup vaults.</span></span>
<span data-ttu-id="18441-107">Этот командлет возвращает объекты **AzureRmBackupVault** для использования с другими командлетами.</span><span class="sxs-lookup"><span data-stu-id="18441-107">This cmdlet returns **AzureRmBackupVault** objects for use with other cmdlets.</span></span>

## <span data-ttu-id="18441-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="18441-108">EXAMPLES</span></span>

### <span data-ttu-id="18441-109">Пример 1: Просмотр всех резервных хранилищ</span><span class="sxs-lookup"><span data-stu-id="18441-109">Example 1: View all the Backup vaults</span></span>
```
PS C:\>Get-AzureRmBackupVault
```

<span data-ttu-id="18441-110">Эта команда получает все резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="18441-110">This command gets all the Azure Backup vaults.</span></span>

### <span data-ttu-id="18441-111">Пример 2: Просмотр всех хранилищ, созданных в Запад США</span><span class="sxs-lookup"><span data-stu-id="18441-111">Example 2: View all vaults created in West US</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Region -eq "westus" }
```

<span data-ttu-id="18441-112">Эта команда возвращает все резервные хранилища.</span><span class="sxs-lookup"><span data-stu-id="18441-112">This command gets all the Backup vaults.</span></span>
<span data-ttu-id="18441-113">Команда передает их в командлет Where-Object с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="18441-113">The command passes them to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="18441-114">Этот командлет фильтрует результаты, основываясь на свойстве **Region** .</span><span class="sxs-lookup"><span data-stu-id="18441-114">That cmdlet filters the results based on the **Region** property.</span></span>
<span data-ttu-id="18441-115">Для получения дополнительных сведений введите `Get-Help Where-Object` .</span><span class="sxs-lookup"><span data-stu-id="18441-115">For more information, type `Get-Help Where-Object`.</span></span>

### <span data-ttu-id="18441-116">Пример 3: получение определенного хранилища</span><span class="sxs-lookup"><span data-stu-id="18441-116">Example 3: Get a specific vault</span></span>
```
PS C:\>Get-AzureRmBackupVault -Name "Vault03"
ResourceId        : /subscriptions/4bfbe168-f42a-4a06-8f5a-331cad1f497e/resourceGroups/ResourceGroup011/providers/Microsoft.Backup
                    /BackupVault/Vault
Name              : Vault03
ResourceGroupName : ResourceGroup01
Region            : westus
Storage           : GeoRedundant
```

<span data-ttu-id="18441-117">Эта команда получает хранилище с именем Vault03.</span><span class="sxs-lookup"><span data-stu-id="18441-117">This command gets the vault named Vault03.</span></span>

### <span data-ttu-id="18441-118">Пример 4: подсчет количества хранилищ с локально избыточным хранилищем</span><span class="sxs-lookup"><span data-stu-id="18441-118">Example 4: Count the number of vaults that have locally redundant storage</span></span>
```
PS C:\>Get-AzureRmBackupVault | Where-Object { $_.Storage -match "LocallyRedundant" } | Measure-Object
Count    : 4
Average  : 
Sum      : 
Maximum  : 
Minimum  : 
Property :
```

<span data-ttu-id="18441-119">Эта команда получает все резервные хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="18441-119">This command gets all the Azure Backup vaults.</span></span>
<span data-ttu-id="18441-120">Команда передает их в **Where-Object** , который фильтрует результаты на основе свойства **Storage** .</span><span class="sxs-lookup"><span data-stu-id="18441-120">The command passes them to **Where-Object** , which filters the results based on the **Storage** property.</span></span>
<span data-ttu-id="18441-121">Команда передается командлету Measure-Object, который содержит значение "LocallyRedundant", в котором учитываются результаты.</span><span class="sxs-lookup"><span data-stu-id="18441-121">The command passes the ones that have a value of LocallyRedundant to the Measure-Object cmdlet, which counts the results.</span></span>
<span data-ttu-id="18441-122">Для получения дополнительных сведений введите `Get-Help Measure-Object` .</span><span class="sxs-lookup"><span data-stu-id="18441-122">For more information, type `Get-Help Measure-Object`.</span></span>

## <span data-ttu-id="18441-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="18441-123">PARAMETERS</span></span>

### <span data-ttu-id="18441-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="18441-124">-Name</span></span>
<span data-ttu-id="18441-125">Указывает имя хранилища резервных копий, которое получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="18441-125">Specifies the name of the Backup vault that this cmdlet gets.</span></span>
<span data-ttu-id="18441-126">Если несколько хранилищ резервных копий имеют одинаковое имя, этот командлет возвращает их все.</span><span class="sxs-lookup"><span data-stu-id="18441-126">If more than one Backup vault has the same name, this cmdlet returns them all.</span></span>
<span data-ttu-id="18441-127">Укажите параметр *ResourceGroupName* , чтобы получить уникальное хранилище.</span><span class="sxs-lookup"><span data-stu-id="18441-127">Specify the *ResourceGroupName* parameter to get a unique vault.</span></span>

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

### <span data-ttu-id="18441-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18441-128">-ResourceGroupName</span></span>
<span data-ttu-id="18441-129">Указывает имя группы ресурсов Azure, в которой этот командлет получает резервное хранилище.</span><span class="sxs-lookup"><span data-stu-id="18441-129">Specifies the name of an Azure resource group in which this cmdlet gets a Backup vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="18441-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18441-130">-DefaultProfile</span></span>
<span data-ttu-id="18441-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="18441-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="18441-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18441-132">CommonParameters</span></span>
<span data-ttu-id="18441-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="18441-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18441-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18441-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18441-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="18441-135">INPUTS</span></span>

## <span data-ttu-id="18441-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="18441-136">OUTPUTS</span></span>

### <span data-ttu-id="18441-137">AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18441-137">AzureRmBackupVault</span></span>

## <span data-ttu-id="18441-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="18441-138">NOTES</span></span>
* <span data-ttu-id="18441-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="18441-139">None</span></span>

## <span data-ttu-id="18441-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="18441-140">RELATED LINKS</span></span>

[<span data-ttu-id="18441-141">Get-AzureRmBackupContainer</span><span class="sxs-lookup"><span data-stu-id="18441-141">Get-AzureRmBackupContainer</span></span>](./Get-AzureRmBackupContainer.md)

[<span data-ttu-id="18441-142">New-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18441-142">New-AzureRmBackupVault</span></span>](./New-AzureRmBackupVault.md)

[<span data-ttu-id="18441-143">Remove-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18441-143">Remove-AzureRmBackupVault</span></span>](./Remove-AzureRmBackupVault.md)

[<span data-ttu-id="18441-144">Set-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="18441-144">Set-AzureRmBackupVault</span></span>](./Set-AzureRmBackupVault.md)


