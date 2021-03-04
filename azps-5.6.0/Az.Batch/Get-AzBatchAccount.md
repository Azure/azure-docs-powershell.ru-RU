---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccount.md
ms.openlocfilehash: 33ada04a3e45c1c8cc9768ef9da98abe781aa01a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959027"
---
# <span data-ttu-id="5d7a6-101">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5d7a6-101">Get-AzBatchAccount</span></span>

## <span data-ttu-id="5d7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="5d7a6-103">Пакетная учетная запись в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-103">Gets a Batch account in the current subscription.</span></span>

## <span data-ttu-id="5d7a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5d7a6-104">SYNTAX</span></span>

```
Get-AzBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d7a6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d7a6-105">DESCRIPTION</span></span>
<span data-ttu-id="5d7a6-106">В текущей подписке для учетной записи **Get-AzBatchAccount** будет учетная запись Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-106">The **Get-AzBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="5d7a6-107">Вы можете использовать параметр *AccountName* для получения одной учетной записи или параметр *ResourceGroupName* для получения учетных записей в этой группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="5d7a6-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5d7a6-108">EXAMPLES</span></span>

### <span data-ttu-id="5d7a6-109">Пример 1. Получить пакетную учетную запись по имени</span><span class="sxs-lookup"><span data-stu-id="5d7a6-109">Example 1: Get a batch account by name</span></span>
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

<span data-ttu-id="5d7a6-110">Эта команда получает пакетную учетную запись с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="5d7a6-111">Пример 2. Получить пакетные учетные записи, связанные с группой ресурсов</span><span class="sxs-lookup"><span data-stu-id="5d7a6-111">Example 2: Get the batch accounts associated with a resource group</span></span>
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

<span data-ttu-id="5d7a6-112">Эта команда получает пакетные учетные записи, связанные с группой ресурсов CmdletExampleRG.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="5d7a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d7a6-113">PARAMETERS</span></span>

### <span data-ttu-id="5d7a6-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5d7a6-114">-AccountName</span></span>
<span data-ttu-id="5d7a6-115">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-115">Specifies the name of an account.</span></span>
<span data-ttu-id="5d7a6-116">Если указать имя учетной записи, этот cmdlet возвращает только эту учетную запись.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-116">If you specify an account name, this cmdlet only returns that account.</span></span>

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

### <span data-ttu-id="5d7a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d7a6-117">-DefaultProfile</span></span>
<span data-ttu-id="5d7a6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5d7a6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d7a6-119">-ResourceGroupName</span></span>
<span data-ttu-id="5d7a6-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-120">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5d7a6-121">При указании группы ресурсов этот cmdlet получает учетные записи в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-121">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

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

### <span data-ttu-id="5d7a6-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="5d7a6-122">-Tag</span></span>
<span data-ttu-id="5d7a6-123">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5d7a6-124">Например: @{key0="value0";key1=$null;key2="value2"} Этот командлет получает учетные записи, содержащие теги, указанные этим параметром.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-124">For example: @{key0="value0";key1=$null;key2="value2"} This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

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

### <span data-ttu-id="5d7a6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d7a6-125">CommonParameters</span></span>
<span data-ttu-id="5d7a6-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d7a6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d7a6-127">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d7a6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d7a6-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5d7a6-128">INPUTS</span></span>

### <span data-ttu-id="5d7a6-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5d7a6-129">System.String</span></span>

### <span data-ttu-id="5d7a6-130">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d7a6-130">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d7a6-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5d7a6-131">OUTPUTS</span></span>

### <span data-ttu-id="5d7a6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5d7a6-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5d7a6-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5d7a6-133">NOTES</span></span>

## <span data-ttu-id="5d7a6-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d7a6-134">RELATED LINKS</span></span>

[<span data-ttu-id="5d7a6-135">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5d7a6-135">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="5d7a6-136">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5d7a6-136">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="5d7a6-137">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5d7a6-137">Set-AzBatchAccount</span></span>](./Set-AzBatchAccount.md)

[<span data-ttu-id="5d7a6-138">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="5d7a6-138">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
