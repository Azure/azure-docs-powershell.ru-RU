---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: FDD2CE98-6C7E-4B95-BA5B-B03B6AC6EAEF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstorageaccountkey
schema: 2.0.0
ms.openlocfilehash: 7ea3847c011582d9be809f030a638b09b6cf9532
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913257"
---
# <span data-ttu-id="baca1-101">New-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="baca1-101">New-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="baca1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baca1-102">SYNOPSIS</span></span>
<span data-ttu-id="baca1-103">Повторное создание ключа хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="baca1-103">Regenerates a storage key for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="baca1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baca1-104">SYNTAX</span></span>

```
New-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="baca1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baca1-105">DESCRIPTION</span></span>
<span data-ttu-id="baca1-106">Командлет **New-AzureRmStorageAccountKey** заново создает ключ хранилища для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="baca1-106">The **New-AzureRmStorageAccountKey** cmdlet regenerates a storage key for an Azure Storage account.</span></span>

## <span data-ttu-id="baca1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baca1-107">EXAMPLES</span></span>

### <span data-ttu-id="baca1-108">Пример 1: повторное создание ключа хранилища</span><span class="sxs-lookup"><span data-stu-id="baca1-108">Example 1: Regenerate a storage key</span></span>
```
PS C:\>New-AzureRmStorageKey -ResourceGroupName "MyResourceGroup" -Name "mystorageaccount" -KeyName "key1"
```

<span data-ttu-id="baca1-109">Эта команда повторно создает ключ хранилища для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="baca1-109">This command regenerates a storage key for the specified Storage account.</span></span>

## <span data-ttu-id="baca1-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baca1-110">PARAMETERS</span></span>

### <span data-ttu-id="baca1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baca1-111">-DefaultProfile</span></span>
<span data-ttu-id="baca1-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baca1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baca1-113">-KeyName</span><span class="sxs-lookup"><span data-stu-id="baca1-113">-KeyName</span></span>
<span data-ttu-id="baca1-114">Указывает, какой ключ нужно повторно создать.</span><span class="sxs-lookup"><span data-stu-id="baca1-114">Specifies which key to regenerate.</span></span>
<span data-ttu-id="baca1-115">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="baca1-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="baca1-116">key1</span><span class="sxs-lookup"><span data-stu-id="baca1-116">key1</span></span>
- <span data-ttu-id="baca1-117">key2</span><span class="sxs-lookup"><span data-stu-id="baca1-117">key2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: key1, key2

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baca1-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baca1-118">-Name</span></span>
<span data-ttu-id="baca1-119">Указывает имя учетной записи хранения, для которой необходимо повторно создать ключ хранилища.</span><span class="sxs-lookup"><span data-stu-id="baca1-119">Specifies the name of the Storage account for which to regenerate a storage key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baca1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baca1-120">-ResourceGroupName</span></span>
<span data-ttu-id="baca1-121">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="baca1-121">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="baca1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baca1-122">CommonParameters</span></span>
<span data-ttu-id="baca1-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baca1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baca1-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baca1-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baca1-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baca1-125">INPUTS</span></span>

### <span data-ttu-id="baca1-126">System. String</span><span class="sxs-lookup"><span data-stu-id="baca1-126">System.String</span></span>

## <span data-ttu-id="baca1-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baca1-127">OUTPUTS</span></span>

### <span data-ttu-id="baca1-128">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="baca1-128">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="baca1-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="baca1-129">NOTES</span></span>

## <span data-ttu-id="baca1-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baca1-130">RELATED LINKS</span></span>

[<span data-ttu-id="baca1-131">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="baca1-131">Get-AzureRmStorageAccountKey</span></span>](./Get-AzureRmStorageAccountKey.md)
