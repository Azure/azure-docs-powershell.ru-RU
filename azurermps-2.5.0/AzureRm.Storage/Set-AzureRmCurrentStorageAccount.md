---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 134af70c3f913d0eec8310f83341de8784f30f25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913715"
---
# <span data-ttu-id="00e94-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00e94-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="00e94-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="00e94-102">SYNOPSIS</span></span>
<span data-ttu-id="00e94-103">Изменение текущей учетной записи хранения для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="00e94-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00e94-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="00e94-104">SYNTAX</span></span>

### <span data-ttu-id="00e94-105">UsingResourceGroupAndNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="00e94-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00e94-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="00e94-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="00e94-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="00e94-107">DESCRIPTION</span></span>
<span data-ttu-id="00e94-108">Командлет **Set-AzureRmCurrentStorageAccount** изменяет текущую учетную запись хранения Azure указанной подписки Azure в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00e94-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="00e94-109">Текущая учетная запись хранилища используется по умолчанию при доступе к хранилищу без указания имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="00e94-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="00e94-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="00e94-110">EXAMPLES</span></span>

### <span data-ttu-id="00e94-111">Пример 1: Настройка текущей учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="00e94-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="00e94-112">Эта команда задает учетную запись хранения по умолчанию для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="00e94-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="00e94-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="00e94-113">PARAMETERS</span></span>

### <span data-ttu-id="00e94-114">-Context</span><span class="sxs-lookup"><span data-stu-id="00e94-114">-Context</span></span>
<span data-ttu-id="00e94-115">Указывает объект **AzureStorageContext** для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="00e94-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="00e94-116">Чтобы получить объект контекста хранилища, используйте командлет New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="00e94-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="00e94-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e94-117">-DefaultProfile</span></span>
<span data-ttu-id="00e94-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="00e94-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e94-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="00e94-119">-Name</span></span>
<span data-ttu-id="00e94-120">Указывает имя учетной записи хранения, которую изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="00e94-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="00e94-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e94-121">-ResourceGroupName</span></span>
<span data-ttu-id="00e94-122">Указывает группу ресурсов, которая содержит учетную запись хранения, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="00e94-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="00e94-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e94-123">CommonParameters</span></span>
<span data-ttu-id="00e94-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="00e94-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e94-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e94-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e94-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="00e94-126">INPUTS</span></span>

### <span data-ttu-id="00e94-127">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="00e94-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="00e94-128">System. String</span><span class="sxs-lookup"><span data-stu-id="00e94-128">System.String</span></span>

## <span data-ttu-id="00e94-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="00e94-129">OUTPUTS</span></span>

### <span data-ttu-id="00e94-130">System. String</span><span class="sxs-lookup"><span data-stu-id="00e94-130">System.String</span></span>

## <span data-ttu-id="00e94-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="00e94-131">NOTES</span></span>

## <span data-ttu-id="00e94-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="00e94-132">RELATED LINKS</span></span>

[<span data-ttu-id="00e94-133">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="00e94-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


