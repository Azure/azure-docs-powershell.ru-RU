---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236785"
---
# <span data-ttu-id="8cbf9-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="8cbf9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cbf9-102">SYNOPSIS</span></span>
<span data-ttu-id="8cbf9-103">Создание новой учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="8cbf9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cbf9-104">SYNTAX</span></span>

### <span data-ttu-id="8cbf9-105">UserOrSystemAssignedEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cbf9-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cbf9-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8cbf9-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cbf9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbf9-107">DESCRIPTION</span></span>
<span data-ttu-id="8cbf9-108">Командлет **New-AzDataLakeStoreAccount** создает новую учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="8cbf9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cbf9-109">EXAMPLES</span></span>

### <span data-ttu-id="8cbf9-110">Пример 1: создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="8cbf9-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="8cbf9-111">Эта команда создает учетную запись Data Lake Store с именем ContosoADL для местоположения "Восток США 2".</span><span class="sxs-lookup"><span data-stu-id="8cbf9-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="8cbf9-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cbf9-112">PARAMETERS</span></span>

### <span data-ttu-id="8cbf9-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="8cbf9-113">-DefaultGroup</span></span>
<span data-ttu-id="8cbf9-114">Указывает идентификатор объекта группы каталогов AzureActive, который будет использоваться по умолчанию владельцем группы для новых файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="8cbf9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cbf9-115">-DefaultProfile</span></span>
<span data-ttu-id="8cbf9-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8cbf9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cbf9-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="8cbf9-117">-DisableEncryption</span></span>
<span data-ttu-id="8cbf9-118">Указывает на то, что для учетной записи не будет применяться ни один из форм шифрования.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="8cbf9-119">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="8cbf9-119">-Encryption</span></span>
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

### <span data-ttu-id="8cbf9-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8cbf9-120">-KeyName</span></span>
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

### <span data-ttu-id="8cbf9-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="8cbf9-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="8cbf9-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8cbf9-122">-KeyVersion</span></span>
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

### <span data-ttu-id="8cbf9-123">-Location</span><span class="sxs-lookup"><span data-stu-id="8cbf9-123">-Location</span></span>
<span data-ttu-id="8cbf9-124">Указывает место, используемое для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="8cbf9-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8cbf9-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cbf9-126">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="8cbf9-126">East US 2</span></span>

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

### <span data-ttu-id="8cbf9-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cbf9-127">-Name</span></span>
<span data-ttu-id="8cbf9-128">Указывает имя создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="8cbf9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cbf9-129">-ResourceGroupName</span></span>
<span data-ttu-id="8cbf9-130">Указывает имя группы ресурсов, которая содержит учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="8cbf9-131">-Тег</span><span class="sxs-lookup"><span data-stu-id="8cbf9-131">-Tag</span></span>
<span data-ttu-id="8cbf9-132">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="8cbf9-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="8cbf9-133">Вы можете использовать теги для идентификации учетной записи Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cbf9-134">Уровень</span><span class="sxs-lookup"><span data-stu-id="8cbf9-134">-Tier</span></span>
<span data-ttu-id="8cbf9-135">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="8cbf9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cbf9-136">CommonParameters</span></span>
<span data-ttu-id="8cbf9-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cbf9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cbf9-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cbf9-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cbf9-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cbf9-139">INPUTS</span></span>

### <span data-ttu-id="8cbf9-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8cbf9-140">System.String</span></span>

### <span data-ttu-id="8cbf9-141">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8cbf9-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="8cbf9-142">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. EncryptionConfigType, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8cbf9-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="8cbf9-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8cbf9-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8cbf9-144">System. Nullable "1 [[Microsoft. Azure. Management. DataStore. Store. TierType, Microsoft. Azure. Management. DataStore. Store, Version = 2.0.0.0, Culture = Neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="8cbf9-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="8cbf9-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cbf9-145">OUTPUTS</span></span>

### <span data-ttu-id="8cbf9-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="8cbf9-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cbf9-147">NOTES</span></span>

## <span data-ttu-id="8cbf9-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cbf9-148">RELATED LINKS</span></span>

[<span data-ttu-id="8cbf9-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8cbf9-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8cbf9-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="8cbf9-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="8cbf9-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)


