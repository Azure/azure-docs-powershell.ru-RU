---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: 2047d8b145296e68d08004b3b2d5f1d20422bfaa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93907038"
---
# <span data-ttu-id="f8e97-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8e97-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="f8e97-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8e97-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e97-103">Получение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="f8e97-103">Gets a Storage account.</span></span>

## <span data-ttu-id="f8e97-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8e97-104">SYNTAX</span></span>

### <span data-ttu-id="f8e97-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8e97-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f8e97-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f8e97-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e97-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e97-107">DESCRIPTION</span></span>
<span data-ttu-id="f8e97-108">Командлет **Get-AzStorageAccount** получает указанную учетную запись хранения или все учетные записи хранения в группе ресурсов или подписке.</span><span class="sxs-lookup"><span data-stu-id="f8e97-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="f8e97-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8e97-109">EXAMPLES</span></span>

### <span data-ttu-id="f8e97-110">Пример 1: получение указанной учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="f8e97-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -Name "mystorageaccount"
```

<span data-ttu-id="f8e97-111">Эта команда получает указанную учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="f8e97-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="f8e97-112">Пример 2: получение всех учетных записей хранения в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="f8e97-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="f8e97-113">Эта команда получает все учетные записи хранения в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8e97-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="f8e97-114">Пример 3: получение всех учетных записей хранения в подписке</span><span class="sxs-lookup"><span data-stu-id="f8e97-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="f8e97-115">Эта команда получает все учетные записи хранения в подписке.</span><span class="sxs-lookup"><span data-stu-id="f8e97-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="f8e97-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8e97-116">PARAMETERS</span></span>

### <span data-ttu-id="f8e97-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e97-117">-DefaultProfile</span></span>
<span data-ttu-id="f8e97-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8e97-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8e97-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f8e97-119">-Name</span></span>
<span data-ttu-id="f8e97-120">Указывает имя учетной записи хранения, которое требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f8e97-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="f8e97-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8e97-121">-ResourceGroupName</span></span>
<span data-ttu-id="f8e97-122">Указывает имя группы ресурсов, которая содержит учетную запись хранения, которую требуется получить.</span><span class="sxs-lookup"><span data-stu-id="f8e97-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="f8e97-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e97-123">CommonParameters</span></span>
<span data-ttu-id="f8e97-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8e97-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e97-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e97-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e97-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8e97-126">INPUTS</span></span>

### <span data-ttu-id="f8e97-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f8e97-127">System.String</span></span>

## <span data-ttu-id="f8e97-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8e97-128">OUTPUTS</span></span>

### <span data-ttu-id="f8e97-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8e97-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="f8e97-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8e97-130">NOTES</span></span>

## <span data-ttu-id="f8e97-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8e97-131">RELATED LINKS</span></span>

[<span data-ttu-id="f8e97-132">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8e97-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="f8e97-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8e97-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="f8e97-134">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f8e97-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


