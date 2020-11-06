---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: c4a8eb0bc75660c13ce8f8492b72cce8a77280e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563752"
---
# <span data-ttu-id="0e59f-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0e59f-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="0e59f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0e59f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e59f-103">Создает пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0e59f-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e59f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0e59f-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e59f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e59f-105">DESCRIPTION</span></span>
<span data-ttu-id="0e59f-106">Командлет **New-AzureRmBatchAccount** создает учетную запись пакета Azure для указанной группы ресурсов и расположения.</span><span class="sxs-lookup"><span data-stu-id="0e59f-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="0e59f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0e59f-107">EXAMPLES</span></span>

### <span data-ttu-id="0e59f-108">Пример 1: создание учетной записи пакетной службы</span><span class="sxs-lookup"><span data-stu-id="0e59f-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="0e59f-109">Эта команда создает пакетную учетную запись с именем pfuller, используя группу ресурсов ResourceGroup03 в области "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="0e59f-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="0e59f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0e59f-110">PARAMETERS</span></span>

### <span data-ttu-id="0e59f-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="0e59f-111">-AccountName</span></span>
<span data-ttu-id="0e59f-112">Указывает имя пакетной учетной записи, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="0e59f-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="0e59f-113">Длина имени учетной записи пакета должна составлять от 3 до 24 символов и содержать только цифры и строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="0e59f-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="0e59f-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="0e59f-115">Указывает идентификатор ресурса для учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="0e59f-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e59f-116">-DefaultProfile</span></span>
<span data-ttu-id="0e59f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0e59f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e59f-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="0e59f-118">-KeyVaultId</span></span>
<span data-ttu-id="0e59f-119">Идентификатор ресурса для хранилища ключей Azure, связанного с пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="0e59f-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0e59f-120">-KeyVaultUrl</span></span>
<span data-ttu-id="0e59f-121">URL-адрес хранилища ключей Azure, связанного с пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="0e59f-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-122">-Location</span><span class="sxs-lookup"><span data-stu-id="0e59f-122">-Location</span></span>
<span data-ttu-id="0e59f-123">Указывает регион, в котором этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0e59f-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="0e59f-124">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="0e59f-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="0e59f-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="0e59f-125">-PoolAllocationMode</span></span>
<span data-ttu-id="0e59f-126">Режим выделения для создания пулов в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="0e59f-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: PoolAllocationMode
Parameter Sets: (All)
Aliases: 
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e59f-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e59f-128">Указывает имя группы ресурсов, в которой этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="0e59f-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="0e59f-129">-Tag</span></span>
<span data-ttu-id="0e59f-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0e59f-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0e59f-131">Например:</span><span class="sxs-lookup"><span data-stu-id="0e59f-131">For example:</span></span>

<span data-ttu-id="0e59f-132">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0e59f-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0e59f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e59f-133">CommonParameters</span></span>
<span data-ttu-id="0e59f-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0e59f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e59f-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e59f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e59f-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0e59f-136">INPUTS</span></span>

### <span data-ttu-id="0e59f-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="0e59f-137">None</span></span>
<span data-ttu-id="0e59f-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0e59f-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e59f-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0e59f-139">OUTPUTS</span></span>

### <span data-ttu-id="0e59f-140">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0e59f-140">BatchAccountContext</span></span>

## <span data-ttu-id="0e59f-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0e59f-141">NOTES</span></span>

## <span data-ttu-id="0e59f-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0e59f-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e59f-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0e59f-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="0e59f-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0e59f-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="0e59f-145">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="0e59f-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="0e59f-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="0e59f-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
