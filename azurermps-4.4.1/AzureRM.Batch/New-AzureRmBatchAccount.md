---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732771"
---
# <span data-ttu-id="4a685-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4a685-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="4a685-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a685-102">SYNOPSIS</span></span>
<span data-ttu-id="4a685-103">Создает пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4a685-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a685-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a685-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a685-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a685-105">DESCRIPTION</span></span>
<span data-ttu-id="4a685-106">Командлет **New-AzureRmBatchAccount** создает учетную запись пакета Azure для указанной группы ресурсов и расположения.</span><span class="sxs-lookup"><span data-stu-id="4a685-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="4a685-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a685-107">EXAMPLES</span></span>

### <span data-ttu-id="4a685-108">Пример 1: создание учетной записи пакетной службы</span><span class="sxs-lookup"><span data-stu-id="4a685-108">Example 1: Create a Batch account</span></span>
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

<span data-ttu-id="4a685-109">Эта команда создает пакетную учетную запись с именем pfuller, используя группу ресурсов ResourceGroup03 в области "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="4a685-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="4a685-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a685-110">PARAMETERS</span></span>

### <span data-ttu-id="4a685-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="4a685-111">-AccountName</span></span>
<span data-ttu-id="4a685-112">Указывает имя пакетной учетной записи, созданной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4a685-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="4a685-113">Длина имени учетной записи пакета должна составлять от 3 до 24 символов и содержать только цифры и строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="4a685-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="4a685-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4a685-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="4a685-115">Указывает идентификатор ресурса для учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="4a685-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="4a685-116">-Location</span><span class="sxs-lookup"><span data-stu-id="4a685-116">-Location</span></span>
<span data-ttu-id="4a685-117">Указывает регион, в котором этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4a685-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="4a685-118">Дополнительные сведения можно найти в разделе [регионы Azure](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="4a685-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="4a685-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a685-119">-ResourceGroupName</span></span>
<span data-ttu-id="4a685-120">Указывает имя группы ресурсов, в которой этот командлет создает учетную запись.</span><span class="sxs-lookup"><span data-stu-id="4a685-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="4a685-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="4a685-121">-Tag</span></span>
<span data-ttu-id="4a685-122">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4a685-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4a685-123">Например:</span><span class="sxs-lookup"><span data-stu-id="4a685-123">For example:</span></span>

<span data-ttu-id="4a685-124">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4a685-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4a685-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a685-125">-DefaultProfile</span></span>
<span data-ttu-id="4a685-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a685-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a685-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a685-127">CommonParameters</span></span>
<span data-ttu-id="4a685-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a685-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a685-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a685-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a685-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a685-130">INPUTS</span></span>

## <span data-ttu-id="4a685-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a685-131">OUTPUTS</span></span>

### <span data-ttu-id="4a685-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4a685-132">BatchAccountContext</span></span>

## <span data-ttu-id="4a685-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a685-133">NOTES</span></span>

## <span data-ttu-id="4a685-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a685-134">RELATED LINKS</span></span>

[<span data-ttu-id="4a685-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4a685-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="4a685-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4a685-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="4a685-137">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="4a685-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="4a685-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="4a685-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
