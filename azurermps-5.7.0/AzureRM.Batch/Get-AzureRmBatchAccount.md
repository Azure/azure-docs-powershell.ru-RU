---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 7fd0283860fd5a0bbca1376afff00c8d4add29b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559316"
---
# <span data-ttu-id="281d4-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="281d4-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="281d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="281d4-102">SYNOPSIS</span></span>
<span data-ttu-id="281d4-103">Возвращает пакетную учетную запись в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="281d4-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="281d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="281d4-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="281d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="281d4-105">DESCRIPTION</span></span>
<span data-ttu-id="281d4-106">Командлет **Get-AzureRmBatchAccount** получает пакетную учетную запись Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="281d4-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="281d4-107">Вы можете использовать параметр *AccountName* для получения одной учетной записи или с помощью параметра *ResourceGroupName* для получения учетных записей в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="281d4-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="281d4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="281d4-108">EXAMPLES</span></span>

### <span data-ttu-id="281d4-109">Пример 1: получение учетной записи пакетной службы по имени</span><span class="sxs-lookup"><span data-stu-id="281d4-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="281d4-110">Эта команда возвращает пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="281d4-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="281d4-111">Пример 2: получение пакетных учетных записей, связанных с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="281d4-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="281d4-112">Эта команда получает учетные записи пакетов, связанные с группой ресурсов CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="281d4-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="281d4-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="281d4-113">PARAMETERS</span></span>

### <span data-ttu-id="281d4-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="281d4-114">-AccountName</span></span>
<span data-ttu-id="281d4-115">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="281d4-115">Specifies the name of an account.</span></span>
<span data-ttu-id="281d4-116">Если указать имя учетной записи, этот командлет вернет только эту учетную запись.</span><span class="sxs-lookup"><span data-stu-id="281d4-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="281d4-117">-DefaultProfile</span></span>
<span data-ttu-id="281d4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="281d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="281d4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="281d4-119">-ResourceGroupName</span></span>
<span data-ttu-id="281d4-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="281d4-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="281d4-121">Если указана группа ресурсов, этот командлет получает учетные записи в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="281d4-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281d4-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="281d4-122">-Tag</span></span>
<span data-ttu-id="281d4-123">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="281d4-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="281d4-124">Например:</span><span class="sxs-lookup"><span data-stu-id="281d4-124">For example:</span></span>

<span data-ttu-id="281d4-125">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="281d4-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="281d4-126">Этот командлет получает учетные записи, содержащие теги, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="281d4-126">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="281d4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="281d4-127">CommonParameters</span></span>
<span data-ttu-id="281d4-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="281d4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="281d4-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="281d4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="281d4-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="281d4-130">INPUTS</span></span>

### <span data-ttu-id="281d4-131">Ничего</span><span class="sxs-lookup"><span data-stu-id="281d4-131">None</span></span>
<span data-ttu-id="281d4-132">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="281d4-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="281d4-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="281d4-133">OUTPUTS</span></span>

### <span data-ttu-id="281d4-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="281d4-134">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="281d4-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="281d4-135">NOTES</span></span>

## <span data-ttu-id="281d4-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="281d4-136">RELATED LINKS</span></span>

[<span data-ttu-id="281d4-137">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="281d4-137">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="281d4-138">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="281d4-138">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="281d4-139">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="281d4-139">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="281d4-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="281d4-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
