---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559315"
---
# <span data-ttu-id="82c55-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="82c55-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="82c55-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="82c55-102">SYNOPSIS</span></span>
<span data-ttu-id="82c55-103">Обновляет пакетную учетную запись.</span><span class="sxs-lookup"><span data-stu-id="82c55-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82c55-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="82c55-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82c55-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c55-105">DESCRIPTION</span></span>
<span data-ttu-id="82c55-106">Командлет **Set-AzureRmBatchAccount** обновляет учетную запись Azure Batch.</span><span class="sxs-lookup"><span data-stu-id="82c55-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="82c55-107">В настоящее время этот командлет может обновлять только теги.</span><span class="sxs-lookup"><span data-stu-id="82c55-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="82c55-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="82c55-108">EXAMPLES</span></span>

### <span data-ttu-id="82c55-109">Пример 1: обновление тегов для учетной записи пакетной службы</span><span class="sxs-lookup"><span data-stu-id="82c55-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
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

<span data-ttu-id="82c55-110">Эта команда обновляет Теги учетной записи с именем pfuller.</span><span class="sxs-lookup"><span data-stu-id="82c55-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="82c55-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="82c55-111">PARAMETERS</span></span>

### <span data-ttu-id="82c55-112">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="82c55-112">-AccountName</span></span>
<span data-ttu-id="82c55-113">Указывает имя пакетной учетной записи, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="82c55-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="82c55-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="82c55-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="82c55-115">Указывает идентификатор ресурса для учетной записи хранения, которая будет использоваться для автоматического хранения.</span><span class="sxs-lookup"><span data-stu-id="82c55-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="82c55-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82c55-116">-DefaultProfile</span></span>
<span data-ttu-id="82c55-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="82c55-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82c55-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82c55-118">-ResourceGroupName</span></span>
<span data-ttu-id="82c55-119">Указывает группу ресурсов для учетной записи, которую обновляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="82c55-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="82c55-120">-Тег</span><span class="sxs-lookup"><span data-stu-id="82c55-120">-Tag</span></span>
<span data-ttu-id="82c55-121">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="82c55-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="82c55-122">Например:</span><span class="sxs-lookup"><span data-stu-id="82c55-122">For example:</span></span>

<span data-ttu-id="82c55-123">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="82c55-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82c55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82c55-124">CommonParameters</span></span>
<span data-ttu-id="82c55-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="82c55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82c55-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82c55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82c55-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="82c55-127">INPUTS</span></span>

### <span data-ttu-id="82c55-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="82c55-128">None</span></span>
<span data-ttu-id="82c55-129">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="82c55-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82c55-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="82c55-130">OUTPUTS</span></span>

### <span data-ttu-id="82c55-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="82c55-131">BatchAccountContext</span></span>

## <span data-ttu-id="82c55-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="82c55-132">NOTES</span></span>

## <span data-ttu-id="82c55-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82c55-133">RELATED LINKS</span></span>

[<span data-ttu-id="82c55-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="82c55-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="82c55-135">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="82c55-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="82c55-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="82c55-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="82c55-137">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="82c55-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
