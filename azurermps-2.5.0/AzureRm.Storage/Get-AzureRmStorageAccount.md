---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
ms.openlocfilehash: dafceede3c3732af423052d33ba125c4ad292d20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913730"
---
# <span data-ttu-id="ea881-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea881-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="ea881-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea881-102">SYNOPSIS</span></span>
<span data-ttu-id="ea881-103">Получение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="ea881-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea881-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea881-104">SYNTAX</span></span>

### <span data-ttu-id="ea881-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea881-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ea881-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea881-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea881-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea881-107">DESCRIPTION</span></span>
<span data-ttu-id="ea881-108">Командлет **Get-AzureRmStorageAccount** получает указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="ea881-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="ea881-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea881-109">EXAMPLES</span></span>

### <span data-ttu-id="ea881-110">Пример 1: получение указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="ea881-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="ea881-111">Эта команда получает указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="ea881-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="ea881-112">Пример 2: получение всех учетных записей хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="ea881-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="ea881-113">Эта команда получает все учетные записи хранения в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea881-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="ea881-114">Пример 3: получение всех учетных записей хранения в подписке</span><span class="sxs-lookup"><span data-stu-id="ea881-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="ea881-115">Эта команда получает все учетные записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="ea881-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="ea881-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea881-116">PARAMETERS</span></span>

### <span data-ttu-id="ea881-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea881-117">-DefaultProfile</span></span>
<span data-ttu-id="ea881-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea881-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea881-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea881-119">-Name</span></span>
<span data-ttu-id="ea881-120">Указывает имя учетной записи хранения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ea881-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea881-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea881-121">-ResourceGroupName</span></span>
<span data-ttu-id="ea881-122">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="ea881-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea881-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea881-123">CommonParameters</span></span>
<span data-ttu-id="ea881-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea881-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea881-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea881-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea881-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea881-126">INPUTS</span></span>

### <span data-ttu-id="ea881-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ea881-127">System.String</span></span>

## <span data-ttu-id="ea881-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea881-128">OUTPUTS</span></span>

### <span data-ttu-id="ea881-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea881-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="ea881-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea881-130">NOTES</span></span>

## <span data-ttu-id="ea881-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea881-131">RELATED LINKS</span></span>

[<span data-ttu-id="ea881-132">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea881-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="ea881-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea881-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="ea881-134">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ea881-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


