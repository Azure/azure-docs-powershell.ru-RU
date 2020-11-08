---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073058"
---
# <span data-ttu-id="096fc-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="096fc-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="096fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="096fc-102">SYNOPSIS</span></span>
<span data-ttu-id="096fc-103">Изменение текущей учетной записи хранения для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="096fc-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="096fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="096fc-104">SYNTAX</span></span>

### <span data-ttu-id="096fc-105">UsingResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="096fc-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="096fc-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="096fc-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="096fc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="096fc-107">DESCRIPTION</span></span>
<span data-ttu-id="096fc-108">Командлет **Set-AzCurrentStorageAccount** изменяет текущую учетную запись хранения Azure указанной подписки Azure в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="096fc-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="096fc-109">Текущая учетная запись хранилища используется по умолчанию при доступе к хранилищу без указания имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="096fc-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="096fc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="096fc-110">EXAMPLES</span></span>

### <span data-ttu-id="096fc-111">Пример 1: Настройка текущей учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="096fc-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="096fc-112">Эта команда задает учетную запись хранения по умолчанию для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="096fc-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="096fc-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="096fc-113">PARAMETERS</span></span>

### <span data-ttu-id="096fc-114">-Context</span><span class="sxs-lookup"><span data-stu-id="096fc-114">-Context</span></span>
<span data-ttu-id="096fc-115">Указывает объект **AzureStorageContext** для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="096fc-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="096fc-116">Чтобы получить объект контекста хранилища, используйте командлет New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="096fc-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="096fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="096fc-117">-DefaultProfile</span></span>
<span data-ttu-id="096fc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="096fc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="096fc-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="096fc-119">-Name</span></span>
<span data-ttu-id="096fc-120">Указывает имя учетной записи хранения, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="096fc-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="096fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="096fc-122">Указывает группу ресурсов, которая содержит учетную запись хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="096fc-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="096fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="096fc-123">CommonParameters</span></span>
<span data-ttu-id="096fc-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="096fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="096fc-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="096fc-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="096fc-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="096fc-126">INPUTS</span></span>

### <span data-ttu-id="096fc-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="096fc-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="096fc-128">System. String</span><span class="sxs-lookup"><span data-stu-id="096fc-128">System.String</span></span>

## <span data-ttu-id="096fc-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="096fc-129">OUTPUTS</span></span>

### <span data-ttu-id="096fc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="096fc-130">System.String</span></span>

## <span data-ttu-id="096fc-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="096fc-131">NOTES</span></span>

## <span data-ttu-id="096fc-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="096fc-132">RELATED LINKS</span></span>

[<span data-ttu-id="096fc-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="096fc-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


