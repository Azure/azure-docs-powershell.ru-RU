---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 66bab11ab5632464eed8ee160df527b0e44f053d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242622"
---
# <span data-ttu-id="7c424-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c424-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="7c424-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c424-102">SYNOPSIS</span></span>
<span data-ttu-id="7c424-103">Возвращает пакетную учетную запись в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7c424-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="7c424-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c424-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c424-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c424-105">DESCRIPTION</span></span>
<span data-ttu-id="7c424-106">Командлет **Get-AzBatchAccount** получает пакетную учетную запись Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="7c424-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="7c424-107">Вы можете использовать параметр *AccountName* для получения одной учетной записи или с помощью параметра *ResourceGroupName* для получения учетных записей в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c424-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="7c424-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c424-108">EXAMPLES</span></span>

### <span data-ttu-id="7c424-109">Пример 1: получение учетной записи пакетной службы по имени</span><span class="sxs-lookup"><span data-stu-id="7c424-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="7c424-110">Эта команда возвращает пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="7c424-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="7c424-111">Пример 2: получение пакетных учетных записей, связанных с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="7c424-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="7c424-112">Эта команда получает учетные записи пакетов, связанные с группой ресурсов CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="7c424-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="7c424-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c424-113">PARAMETERS</span></span>

### <span data-ttu-id="7c424-114">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="7c424-114">-AccountName</span></span>
<span data-ttu-id="7c424-115">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7c424-115">Specifies the name of an account.</span></span>
<span data-ttu-id="7c424-116">Если указать имя учетной записи, этот командлет вернет только эту учетную запись.</span><span class="sxs-lookup"><span data-stu-id="7c424-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c424-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c424-117">-DefaultProfile</span></span>
<span data-ttu-id="7c424-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c424-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c424-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c424-119">-ResourceGroupName</span></span>
<span data-ttu-id="7c424-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c424-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="7c424-121">Если указана группа ресурсов, этот командлет получает учетные записи в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c424-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c424-122">-Тег</span><span class="sxs-lookup"><span data-stu-id="7c424-122">-Tag</span></span>
<span data-ttu-id="7c424-123">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c424-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7c424-124">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"} Этот командлет получает учетные записи, содержащие теги, которые указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="7c424-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c424-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c424-125">CommonParameters</span></span>
<span data-ttu-id="7c424-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c424-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c424-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c424-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c424-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c424-128">INPUTS</span></span>

### <span data-ttu-id="7c424-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7c424-129">System.String</span></span>

### <span data-ttu-id="7c424-130">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="7c424-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="7c424-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c424-131">OUTPUTS</span></span>

### <span data-ttu-id="7c424-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7c424-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7c424-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c424-133">NOTES</span></span>

## <span data-ttu-id="7c424-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c424-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c424-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c424-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="7c424-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c424-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="7c424-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="7c424-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="7c424-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="7c424-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)