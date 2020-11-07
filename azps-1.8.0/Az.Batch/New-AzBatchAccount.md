---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchAccount.md
ms.openlocfilehash: e996e02c9609e259c0833cfe179f295206684351
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731864"
---
# <span data-ttu-id="058ca-101">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="058ca-101">New-AzBatchAccount</span></span>

## <span data-ttu-id="058ca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="058ca-102">SYNOPSIS</span></span>
<span data-ttu-id="058ca-103">Создает пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="058ca-103">Creates a Batch account.</span></span>

## <span data-ttu-id="058ca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="058ca-104">SYNTAX</span></span>

```
New-AzBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="058ca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="058ca-105">DESCRIPTION</span></span>
<span data-ttu-id="058ca-106">Командлет **New-AzBatchAccount** создает учетную запись пакета Azure для указанной группы ресурсов и расположения.</span><span class="sxs-lookup"><span data-stu-id="058ca-106">The **New-AzBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="058ca-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="058ca-107">EXAMPLES</span></span>

### <span data-ttu-id="058ca-108">Пример 1: создание учетной записи пакетной службы</span><span class="sxs-lookup"><span data-stu-id="058ca-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="058ca-109">Эта команда создает пакетную учетную запись с именем pfuller, используя группу ресурсов ResourceGroup03 в области "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="058ca-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="058ca-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="058ca-110">PARAMETERS</span></span>

### <span data-ttu-id="058ca-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="058ca-111">-AccountName</span></span>
<span data-ttu-id="058ca-112">Указывает имя пакетной учетной записи, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="058ca-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="058ca-113">Длина имени учетной записи пакета должна составлять от 3 до 24 символов и содержать только цифры и строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="058ca-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058ca-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="058ca-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="058ca-115">Указывает идентификатор ресурса для учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="058ca-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="058ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="058ca-116">-DefaultProfile</span></span>
<span data-ttu-id="058ca-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="058ca-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="058ca-118">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="058ca-118">-KeyVaultId</span></span>
<span data-ttu-id="058ca-119">Идентификатор ресурса для хранилища ключей Azure, связанного с пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="058ca-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058ca-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="058ca-120">-KeyVaultUrl</span></span>
<span data-ttu-id="058ca-121">URL-адрес хранилища ключей Azure, связанного с пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="058ca-121">The URL of the Azure key vault associated with the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058ca-122">-Location</span><span class="sxs-lookup"><span data-stu-id="058ca-122">-Location</span></span>
<span data-ttu-id="058ca-123">Указывает регион, в котором этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="058ca-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="058ca-124">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="058ca-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="058ca-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="058ca-125">-PoolAllocationMode</span></span>
<span data-ttu-id="058ca-126">Режим выделения для создания пулов в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="058ca-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="058ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="058ca-128">Указывает имя группы ресурсов, в которой этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="058ca-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="058ca-129">-Тег</span><span class="sxs-lookup"><span data-stu-id="058ca-129">-Tag</span></span>
<span data-ttu-id="058ca-130">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="058ca-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="058ca-131">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="058ca-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="058ca-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="058ca-132">CommonParameters</span></span>
<span data-ttu-id="058ca-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="058ca-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="058ca-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="058ca-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="058ca-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="058ca-135">INPUTS</span></span>

### <span data-ttu-id="058ca-136">System. String</span><span class="sxs-lookup"><span data-stu-id="058ca-136">System.String</span></span>

### <span data-ttu-id="058ca-137">System. Nullable "1 [[Microsoft.Azure.Management.BatCH. Models. PoolAllocationMode, Microsoft.Azure.Management.BatCH, версия = 4.0.0.0, культура = нейтральная, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="058ca-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="058ca-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="058ca-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="058ca-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="058ca-139">OUTPUTS</span></span>

### <span data-ttu-id="058ca-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="058ca-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="058ca-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="058ca-141">NOTES</span></span>

## <span data-ttu-id="058ca-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="058ca-142">RELATED LINKS</span></span>

[<span data-ttu-id="058ca-143">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="058ca-143">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="058ca-144">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="058ca-144">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="058ca-145">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="058ca-145">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="058ca-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="058ca-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)
