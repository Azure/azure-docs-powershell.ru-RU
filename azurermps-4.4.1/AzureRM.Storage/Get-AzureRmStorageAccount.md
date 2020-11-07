---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732560"
---
# <span data-ttu-id="f2a00-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2a00-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="f2a00-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2a00-102">SYNOPSIS</span></span>
<span data-ttu-id="f2a00-103">Получение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f2a00-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2a00-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2a00-104">SYNTAX</span></span>

### <span data-ttu-id="f2a00-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a00-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2a00-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f2a00-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2a00-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2a00-107">DESCRIPTION</span></span>
<span data-ttu-id="f2a00-108">Командлет **Get-AzureRmStorageAccount** получает указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="f2a00-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="f2a00-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2a00-109">EXAMPLES</span></span>

### <span data-ttu-id="f2a00-110">Пример 1: получение указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f2a00-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="f2a00-111">Эта команда получает указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="f2a00-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="f2a00-112">Пример 2: получение всех учетных записей хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f2a00-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="f2a00-113">Эта команда получает все учетные записи хранения в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f2a00-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="f2a00-114">Пример 3: получение всех учетных записей хранения в подписке</span><span class="sxs-lookup"><span data-stu-id="f2a00-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="f2a00-115">Эта команда получает все учетные записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="f2a00-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="f2a00-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2a00-116">PARAMETERS</span></span>

### <span data-ttu-id="f2a00-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f2a00-117">-Name</span></span>
<span data-ttu-id="f2a00-118">Указывает имя учетной записи хранения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f2a00-118">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="f2a00-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2a00-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2a00-120">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f2a00-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="f2a00-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2a00-121">-DefaultProfile</span></span>
<span data-ttu-id="f2a00-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f2a00-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2a00-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2a00-123">CommonParameters</span></span>
<span data-ttu-id="f2a00-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2a00-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2a00-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2a00-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2a00-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2a00-126">INPUTS</span></span>

## <span data-ttu-id="f2a00-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2a00-127">OUTPUTS</span></span>

## <span data-ttu-id="f2a00-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2a00-128">NOTES</span></span>

## <span data-ttu-id="f2a00-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2a00-129">RELATED LINKS</span></span>

[<span data-ttu-id="f2a00-130">New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2a00-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="f2a00-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2a00-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="f2a00-132">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f2a00-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


