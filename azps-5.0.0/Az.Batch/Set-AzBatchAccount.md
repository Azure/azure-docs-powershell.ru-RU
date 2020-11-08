---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249109"
---
# <span data-ttu-id="b7a25-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7a25-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="b7a25-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b7a25-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a25-103">Обновляет пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="b7a25-103">Updates a Batch account.</span></span>

## <span data-ttu-id="b7a25-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b7a25-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7a25-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a25-105">DESCRIPTION</span></span>
<span data-ttu-id="b7a25-106">Командлет **Set-AzBatchAccount** обновляет учетную запись Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="b7a25-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="b7a25-107">В настоящее время этот командлет может обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="b7a25-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="b7a25-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b7a25-108">EXAMPLES</span></span>

### <span data-ttu-id="b7a25-109">Пример 1: обновление тегов для учетной записи пакетной службы</span><span class="sxs-lookup"><span data-stu-id="b7a25-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
DedicatedCoreQuota           : 20
LowPriorityCoreQuota         : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="b7a25-110">Эта команда обновляет Теги учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="b7a25-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="b7a25-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b7a25-111">PARAMETERS</span></span>

### <span data-ttu-id="b7a25-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="b7a25-112">-AccountName</span></span>
<span data-ttu-id="b7a25-113">Указывает имя пакетной учетной записи, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b7a25-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b7a25-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b7a25-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="b7a25-115">Указывает идентификатор ресурса для учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="b7a25-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="b7a25-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a25-116">-DefaultProfile</span></span>
<span data-ttu-id="b7a25-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7a25-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7a25-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a25-118">-ResourceGroupName</span></span>
<span data-ttu-id="b7a25-119">Указывает группу ресурсов для учетной записи, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b7a25-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="b7a25-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="b7a25-120">-Tag</span></span>
<span data-ttu-id="b7a25-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b7a25-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b7a25-122">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b7a25-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7a25-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a25-123">CommonParameters</span></span>
<span data-ttu-id="b7a25-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b7a25-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a25-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7a25-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a25-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b7a25-126">INPUTS</span></span>

### <span data-ttu-id="b7a25-127">System. String</span><span class="sxs-lookup"><span data-stu-id="b7a25-127">System.String</span></span>

### <span data-ttu-id="b7a25-128">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7a25-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7a25-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7a25-129">OUTPUTS</span></span>

### <span data-ttu-id="b7a25-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b7a25-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b7a25-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="b7a25-131">NOTES</span></span>

## <span data-ttu-id="b7a25-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7a25-132">RELATED LINKS</span></span>

[<span data-ttu-id="b7a25-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7a25-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="b7a25-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7a25-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="b7a25-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="b7a25-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="b7a25-136">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b7a25-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
