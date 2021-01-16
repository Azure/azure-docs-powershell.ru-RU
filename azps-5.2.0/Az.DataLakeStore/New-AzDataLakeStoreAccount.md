---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 58AAA284-45A3-4360-B321-FBE0A3F5D7A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreAccount.md
ms.openlocfilehash: 4bdf13b485486a8e3c40023ea0011d12b21a93b8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415031"
---
# <span data-ttu-id="3aa43-101">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-101">New-AzDataLakeStoreAccount</span></span>

## <span data-ttu-id="3aa43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3aa43-102">SYNOPSIS</span></span>
<span data-ttu-id="3aa43-103">Создает новую учетную запись Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3aa43-103">Creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="3aa43-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3aa43-104">SYNTAX</span></span>

### <span data-ttu-id="3aa43-105">UserOrSystemAssignedEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3aa43-105">UserOrSystemAssignedEncryption (Default)</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [[-Encryption] <EncryptionConfigType>]
 [[-KeyVaultId] <String>] [[-KeyName] <String>] [[-KeyVersion] <String>] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3aa43-106">DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="3aa43-106">DisableEncryption</span></span>
```
New-AzDataLakeStoreAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-DefaultGroup] <String>] [[-Tag] <Hashtable>] [-DisableEncryption] [-Tier <TierType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3aa43-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3aa43-107">DESCRIPTION</span></span>
<span data-ttu-id="3aa43-108">Для создания учетной записи Data Lake Store будет создаваться новый **cmdlet AzDataLakeStoreAccount.**</span><span class="sxs-lookup"><span data-stu-id="3aa43-108">The **New-AzDataLakeStoreAccount** cmdlet creates a new Data Lake Store account.</span></span>

## <span data-ttu-id="3aa43-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3aa43-109">EXAMPLES</span></span>

### <span data-ttu-id="3aa43-110">Пример 1. Создание учетной записи</span><span class="sxs-lookup"><span data-stu-id="3aa43-110">Example 1: Create an account</span></span>
```
PS C:\>New-AzDataLakeStoreAccount -Name "ContosoADL" -ResourceGroupName "ContosoOrg" -Location "East US 2"
```

<span data-ttu-id="3aa43-111">Эта команда создает учетную запись Магазина данных с именем ContosoADL для расположения на востоке США.</span><span class="sxs-lookup"><span data-stu-id="3aa43-111">This command creates a Data Lake Store account named ContosoADL for the East US 2 location.</span></span>

## <span data-ttu-id="3aa43-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3aa43-112">PARAMETERS</span></span>

### <span data-ttu-id="3aa43-113">-DefaultGroup</span><span class="sxs-lookup"><span data-stu-id="3aa43-113">-DefaultGroup</span></span>
<span data-ttu-id="3aa43-114">Определяет ИД объекта группы AzureActive Directory, который будет по умолчанию владельцем группы для новых файлов и папок.</span><span class="sxs-lookup"><span data-stu-id="3aa43-114">Specifies the object ID of the AzureActive Directory group to use as the default group owner for new files and folders.</span></span>

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

### <span data-ttu-id="3aa43-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aa43-115">-DefaultProfile</span></span>
<span data-ttu-id="3aa43-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3aa43-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3aa43-117">-DisableEncryption</span><span class="sxs-lookup"><span data-stu-id="3aa43-117">-DisableEncryption</span></span>
<span data-ttu-id="3aa43-118">Означает, что к учетной записи не будет применено шифрование.</span><span class="sxs-lookup"><span data-stu-id="3aa43-118">Indicates that the account will not have any form of encryption applied to it.</span></span>

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

### <span data-ttu-id="3aa43-119">-Encryption</span><span class="sxs-lookup"><span data-stu-id="3aa43-119">-Encryption</span></span>
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

### <span data-ttu-id="3aa43-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3aa43-120">-KeyName</span></span>
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

### <span data-ttu-id="3aa43-121">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3aa43-121">-KeyVaultId</span></span>
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

### <span data-ttu-id="3aa43-122">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3aa43-122">-KeyVersion</span></span>
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

### <span data-ttu-id="3aa43-123">-Location</span><span class="sxs-lookup"><span data-stu-id="3aa43-123">-Location</span></span>
<span data-ttu-id="3aa43-124">Определяет расположение для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3aa43-124">Specifies the location to use for the account.</span></span>
<span data-ttu-id="3aa43-125">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="3aa43-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3aa43-126">Восток США 2</span><span class="sxs-lookup"><span data-stu-id="3aa43-126">East US 2</span></span>

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

### <span data-ttu-id="3aa43-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3aa43-127">-Name</span></span>
<span data-ttu-id="3aa43-128">Указывает имя создаемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3aa43-128">Specifies the name of the account to create.</span></span>

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

### <span data-ttu-id="3aa43-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aa43-129">-ResourceGroupName</span></span>
<span data-ttu-id="3aa43-130">Имя группы ресурсов, которая содержит учетную запись.</span><span class="sxs-lookup"><span data-stu-id="3aa43-130">Specifies the name of the resource group that contains the account.</span></span>

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

### <span data-ttu-id="3aa43-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="3aa43-131">-Tag</span></span>
<span data-ttu-id="3aa43-132">Теги в качестве пар значений ключа.</span><span class="sxs-lookup"><span data-stu-id="3aa43-132">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="3aa43-133">С помощью тегов можно определить учетную запись Data Lake Store из других ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3aa43-133">You can use tags to identify a Data Lake Store account from other Azure resources.</span></span>

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

### <span data-ttu-id="3aa43-134">-Tier</span><span class="sxs-lookup"><span data-stu-id="3aa43-134">-Tier</span></span>
<span data-ttu-id="3aa43-135">Нужный уровень обязательств для этой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="3aa43-135">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="3aa43-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aa43-136">CommonParameters</span></span>
<span data-ttu-id="3aa43-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3aa43-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aa43-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3aa43-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aa43-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3aa43-139">INPUTS</span></span>

### <span data-ttu-id="3aa43-140">System.String</span><span class="sxs-lookup"><span data-stu-id="3aa43-140">System.String</span></span>

### <span data-ttu-id="3aa43-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3aa43-141">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3aa43-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3aa43-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.EncryptionConfigType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="3aa43-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3aa43-143">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3aa43-144">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3aa43-144">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Store.Models.TierType, Microsoft.Azure.Management.DataLake.Store, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3aa43-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3aa43-145">OUTPUTS</span></span>

### <span data-ttu-id="3aa43-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDAtaLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-146">Microsoft.Azure.Commands.DataLakeStore.Models.PSDataLakeStoreAccount</span></span>

## <span data-ttu-id="3aa43-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3aa43-147">NOTES</span></span>

## <span data-ttu-id="3aa43-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3aa43-148">RELATED LINKS</span></span>

[<span data-ttu-id="3aa43-149">Get-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-149">Get-AzDataLakeStoreAccount</span></span>](./Get-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3aa43-150">Remove-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-150">Remove-AzDataLakeStoreAccount</span></span>](./Remove-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3aa43-151">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-151">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

[<span data-ttu-id="3aa43-152">Test-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3aa43-152">Test-AzDataLakeStoreAccount</span></span>](./Test-AzDataLakeStoreAccount.md)

