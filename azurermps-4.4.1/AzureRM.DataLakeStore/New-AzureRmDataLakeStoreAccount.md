---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: b05cb9e3789afa905da93642929f65f4965f9b0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93735183"
---
# <span data-ttu-id="98641-101">New-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-101">New-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="98641-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="98641-102">SYNOPSIS</span></span>
<span data-ttu-id="98641-103">Создание новой учетной записи для Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="98641-103">Creates a new Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98641-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="98641-104">SYNTAX</span></span>

### <span data-ttu-id="98641-105">Шифрование, назначенное пользователем или системой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="98641-105">User or System assigned encryption (Default)</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="98641-106">Отключить шифрование</span><span class="sxs-lookup"><span data-stu-id="98641-106">Disable Encryption</span></span>
```
New-AzureRmDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tags] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98641-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="98641-107">DESCRIPTION</span></span>
<span data-ttu-id="98641-108">Командлет **New-AzureRmDataLakeStoreAccount** создает новую учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="98641-108">The **New-AzureRmDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="98641-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="98641-109">EXAMPLES</span></span>

### <span data-ttu-id="98641-110">Пример 1: создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="98641-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzureRmDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="98641-111">Эта команда создает учетную запись Data Lake Store с именем ContosoADL для местоположения "Восток США 2".</span><span class="sxs-lookup"><span data-stu-id="98641-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="98641-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="98641-112">PARAMETERS</span></span>

### <span data-ttu-id="98641-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="98641-113">-DefaultGroup</span></span>
<span data-ttu-id="98641-114">Указывает идентификатор объекта группы каталогов AzureActive, который будет использоваться по умолчанию владельцем группы для новых файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="98641-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="98641-115">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="98641-115">-DisableEncryption</span></span>
<span data-ttu-id="98641-116">Указывает на то, что для учетной записи не будет применяться ни один из форм шифрования.</span><span class="sxs-lookup"><span data-stu-id="98641-116">Indicates that the account will not have any form of encryption applied to it.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable Encryption
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98641-117">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="98641-117">-Encryption</span></span>
```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType]
Parameter Sets: User or System assigned encryption
Aliases: 
Accepted values: UserManaged, ServiceManaged

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98641-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="98641-118">-KeyName</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98641-119">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="98641-119">-KeyVaultId</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98641-120">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="98641-120">-KeyVersion</span></span>
```yaml
Type: System.String
Parameter Sets: User or System assigned encryption
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98641-121">-Location</span><span class="sxs-lookup"><span data-stu-id="98641-121">-Location</span></span>
<span data-ttu-id="98641-122">Указывает место, используемое для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98641-122">Specifies the location to use for the account.</span></span>
<span data-ttu-id="98641-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="98641-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98641-124">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="98641-124">East US 2</span></span>

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

### <span data-ttu-id="98641-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="98641-125">-Name</span></span>
<span data-ttu-id="98641-126">Указывает имя создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98641-126">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="98641-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98641-127">-ResourceGroupName</span></span>
<span data-ttu-id="98641-128">Указывает имя группы ресурсов, которая содержит учетную запись.</span><span class="sxs-lookup"><span data-stu-id="98641-128">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="98641-129">-Теги</span><span class="sxs-lookup"><span data-stu-id="98641-129">-Tags</span></span>
<span data-ttu-id="98641-130">Определяет теги как пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="98641-130">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="98641-131">Вы можете использовать теги для идентификации учетной записи Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="98641-131">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="98641-132">Уровень</span><span class="sxs-lookup"><span data-stu-id="98641-132">-Tier</span></span>
<span data-ttu-id="98641-133">Требуемый уровень обязательства для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98641-133">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="98641-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98641-134">-DefaultProfile</span></span>
<span data-ttu-id="98641-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="98641-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98641-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98641-136">CommonParameters</span></span>
<span data-ttu-id="98641-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="98641-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98641-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98641-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98641-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="98641-139">INPUTS</span></span>

## <span data-ttu-id="98641-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="98641-140">OUTPUTS</span></span>

### <span data-ttu-id="98641-141">PSDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-141">PSDataLakeStoreAccount</span></span>
<span data-ttu-id="98641-142">Сведения о созданной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="98641-142">The created account details.</span></span>

## <span data-ttu-id="98641-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="98641-143">NOTES</span></span>

## <span data-ttu-id="98641-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="98641-144">RELATED LINKS</span></span>

[<span data-ttu-id="98641-145">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-145">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="98641-146">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-146">Remove-AzureRmDataLakeStoreAccount</span></span>](./Remove-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="98641-147">Set-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-147">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="98641-148">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="98641-148">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


