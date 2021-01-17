---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchAccount.md
ms.openlocfilehash: 44627bd5ffa7340a10866605598d981b10f35a58
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393623"
---
# <span data-ttu-id="8e487-101">Set-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8e487-101">Set-AzBatchAccount</span></span>

## <span data-ttu-id="8e487-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e487-102">SYNOPSIS</span></span>
<span data-ttu-id="8e487-103">Обновляет учетную запись пакета.</span><span class="sxs-lookup"><span data-stu-id="8e487-103">Updates a Batch account.</span></span>

## <span data-ttu-id="8e487-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8e487-104">SYNTAX</span></span>

```
Set-AzBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e487-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8e487-105">DESCRIPTION</span></span>
<span data-ttu-id="8e487-106">Для учетной записи Azure Batch обновляется **cmdlet Set-AzBatchAccount.**</span><span class="sxs-lookup"><span data-stu-id="8e487-106">The **Set-AzBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="8e487-107">В настоящее время этот командлет может обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="8e487-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="8e487-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8e487-108">EXAMPLES</span></span>

### <span data-ttu-id="8e487-109">Пример 1. Обновление тегов в учетной записи пакета</span><span class="sxs-lookup"><span data-stu-id="8e487-109">Example 1: Update the tags on a Batch account</span></span>
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

<span data-ttu-id="8e487-110">Эта команда обновляет теги для учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="8e487-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="8e487-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e487-111">PARAMETERS</span></span>

### <span data-ttu-id="8e487-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8e487-112">-AccountName</span></span>
<span data-ttu-id="8e487-113">Имя учетной записи пакета, которую обновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e487-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8e487-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8e487-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="8e487-115">Определяет ИД ресурса учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="8e487-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="8e487-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e487-116">-DefaultProfile</span></span>
<span data-ttu-id="8e487-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8e487-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e487-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e487-118">-ResourceGroupName</span></span>
<span data-ttu-id="8e487-119">Определяет группу ресурсов учетной записи, которую обновляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e487-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="8e487-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="8e487-120">-Tag</span></span>
<span data-ttu-id="8e487-121">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="8e487-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8e487-122">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8e487-122">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8e487-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e487-123">CommonParameters</span></span>
<span data-ttu-id="8e487-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e487-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e487-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e487-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e487-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e487-126">INPUTS</span></span>

### <span data-ttu-id="8e487-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8e487-127">System.String</span></span>

### <span data-ttu-id="8e487-128">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="8e487-128">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8e487-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8e487-129">OUTPUTS</span></span>

### <span data-ttu-id="8e487-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8e487-130">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="8e487-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8e487-131">NOTES</span></span>

## <span data-ttu-id="8e487-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8e487-132">RELATED LINKS</span></span>

[<span data-ttu-id="8e487-133">Get-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8e487-133">Get-AzBatchAccount</span></span>](./Get-AzBatchAccount.md)

[<span data-ttu-id="8e487-134">New-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8e487-134">New-AzBatchAccount</span></span>](./New-AzBatchAccount.md)

[<span data-ttu-id="8e487-135">Remove-AzBatchAccount</span><span class="sxs-lookup"><span data-stu-id="8e487-135">Remove-AzBatchAccount</span></span>](./Remove-AzBatchAccount.md)

[<span data-ttu-id="8e487-136">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="8e487-136">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
