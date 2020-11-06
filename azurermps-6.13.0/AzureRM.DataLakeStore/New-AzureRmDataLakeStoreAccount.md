---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/new-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 3a3e2ea1fdac71759de7278ed34666e3a756ccca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556703"
---
# <span data-ttu-id="19d91-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="19d91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="19d91-102">SYNOPSIS</span></span>
<span data-ttu-id="19d91-103">Создание новой учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19d91-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19d91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="19d91-104">SYNTAX</span></span>

### <span data-ttu-id="19d91-105">UserOrSystemAssignedEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19d91-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19d91-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="19d91-106">DisableEncryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19d91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19d91-107">DESCRIPTION</span></span>
<span data-ttu-id="19d91-108">Командлет **New-AzureRmDataLakeStoreAccount** создает новую учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="19d91-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="19d91-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="19d91-109">EXAMPLES</span></span>

### <span data-ttu-id="19d91-110">Пример 1: создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="19d91-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="19d91-111">Эта команда создает учетную запись Data Lake Store с именем ContosoADL для местоположения "Восток США 2".</span><span class="sxs-lookup"><span data-stu-id="19d91-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="19d91-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="19d91-112">PARAMETERS</span></span>

### <span data-ttu-id="19d91-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="19d91-113">-DefaultGroup</span></span>
<span data-ttu-id="19d91-114">Указывает идентификатор объекта группы каталогов AzureActive, который будет использоваться по умолчанию владельцем группы для новых файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="19d91-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19d91-115">-DefaultProfile</span></span>
<span data-ttu-id="19d91-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="19d91-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19d91-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="19d91-117">-DisableEncryption</span></span>
<span data-ttu-id="19d91-118">Указывает на то, что для учетной записи не будет применяться ни один из форм шифрования.</span><span class="sxs-lookup"><span data-stu-id="19d91-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEncryption
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-119">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="19d91-119">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="19d91-120">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="19d91-121">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="19d91-122">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: UserOrSystemAssignedEncryption
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-123">-Location</span><span class="sxs-lookup"><span data-stu-id="19d91-123">-Location</span></span>
<span data-ttu-id="19d91-124">Указывает место, используемое для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="19d91-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="19d91-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="19d91-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="19d91-126">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="19d91-126">East US 2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="19d91-127">-Name</span></span>
<span data-ttu-id="19d91-128">Указывает имя создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="19d91-128">Specifies the name of the account to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19d91-129">-ResourceGroupName</span></span>
<span data-ttu-id="19d91-130">Указывает имя группы ресурсов, которая содержит учетную запись.</span><span class="sxs-lookup"><span data-stu-id="19d91-130">Specifies the name of the resource group that contains the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="19d91-131">-Tag</span></span>
<span data-ttu-id="19d91-132">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="19d91-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="19d91-133">Вы можете использовать теги для идентификации учетной записи Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="19d91-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-134">Уровень</span><span class="sxs-lookup"><span data-stu-id="19d91-134">-Tier</span></span>
<span data-ttu-id="19d91-135">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="19d91-135">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment1TB, Commitment10TB, Commitment100TB, Commitment500TB, Commitment1PB, Commitment5PB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19d91-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19d91-136">CommonParameters</span></span>
<span data-ttu-id="19d91-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="19d91-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19d91-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19d91-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19d91-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="19d91-139">INPUTS</span></span>

### <span data-ttu-id="19d91-140">System. String</span><span class="sxs-lookup"><span data-stu-id="19d91-140">System.String</span></span>

### <span data-ttu-id="19d91-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="19d91-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="19d91-142">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. EncryptionConfigType, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="19d91-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="19d91-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19d91-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="19d91-144">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. TierType, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="19d91-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="19d91-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="19d91-145">OUTPUTS</span></span>

### <span data-ttu-id="19d91-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="19d91-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="19d91-147">NOTES</span></span>

## <span data-ttu-id="19d91-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19d91-148">RELATED LINKS</span></span>

[<span data-ttu-id="19d91-149">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-149">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="19d91-150">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-150">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="19d91-151">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-151">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="19d91-152">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="19d91-152">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


