---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732673"
---
# <span data-ttu-id="b831d-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b831d-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="b831d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b831d-102">SYNOPSIS</span></span>
<span data-ttu-id="b831d-103">Изменение текущей учетной записи хранения для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="b831d-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b831d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b831d-104">SYNTAX</span></span>

### <span data-ttu-id="b831d-105">UsingResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b831d-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b831d-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="b831d-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b831d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b831d-107">DESCRIPTION</span></span>
<span data-ttu-id="b831d-108">Командлет **Set-AzureRmCurrentStorageAccount** изменяет текущую учетную запись хранения Azure указанной подписки Azure в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="b831d-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="b831d-109">Текущая учетная запись хранилища используется по умолчанию при доступе к хранилищу без указания имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b831d-109">The current storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="b831d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b831d-110">EXAMPLES</span></span>

### <span data-ttu-id="b831d-111">Пример 1: Настройка текущей учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="b831d-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="b831d-112">Эта команда задает учетную запись хранения по умолчанию для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="b831d-112">This command sets the default storage account for the specified subscription.</span></span>

## <span data-ttu-id="b831d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b831d-113">PARAMETERS</span></span>

### <span data-ttu-id="b831d-114">-Context</span><span class="sxs-lookup"><span data-stu-id="b831d-114">-Context</span></span>
<span data-ttu-id="b831d-115">Указывает объект **AzureStorageContext** для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="b831d-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="b831d-116">Чтобы получить объект контекста хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b831d-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b831d-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b831d-117">-Name</span></span>
<span data-ttu-id="b831d-118">Указывает имя учетной записи хранения, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b831d-118">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="b831d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b831d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b831d-120">Указывает группу ресурсов, которая содержит учетную запись хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="b831d-120">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="b831d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b831d-121">-DefaultProfile</span></span>
<span data-ttu-id="b831d-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b831d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b831d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b831d-123">CommonParameters</span></span>
<span data-ttu-id="b831d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b831d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b831d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b831d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b831d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b831d-126">INPUTS</span></span>

## <span data-ttu-id="b831d-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b831d-127">OUTPUTS</span></span>

## <span data-ttu-id="b831d-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b831d-128">NOTES</span></span>

## <span data-ttu-id="b831d-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b831d-129">RELATED LINKS</span></span>

[<span data-ttu-id="b831d-130">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b831d-130">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


