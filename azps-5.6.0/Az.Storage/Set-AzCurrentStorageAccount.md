---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101950787"
---
# <span data-ttu-id="737a6-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="737a6-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="737a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737a6-102">SYNOPSIS</span></span>
<span data-ttu-id="737a6-103">Изменяет текущую учетную запись хранения указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="737a6-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="737a6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="737a6-104">SYNTAX</span></span>

### <span data-ttu-id="737a6-105">UsingResourceGroupAndNameParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="737a6-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737a6-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="737a6-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="737a6-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="737a6-107">DESCRIPTION</span></span>
<span data-ttu-id="737a6-108">**Cmdlet Set-AzCurrentStorageAccount** изменяет текущую учетную запись хранилища Azure для указанной подписки Azure в Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="737a6-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="737a6-109">Текущая учетная запись хранения используется по умолчанию при доступе к хранилищу без указания имени учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="737a6-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="737a6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="737a6-110">EXAMPLES</span></span>

### <span data-ttu-id="737a6-111">Пример 1. Настройка текущей учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="737a6-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="737a6-112">Эта команда задает учетную запись хранения по умолчанию для указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="737a6-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="737a6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="737a6-113">PARAMETERS</span></span>

### <span data-ttu-id="737a6-114">-Контекст</span><span class="sxs-lookup"><span data-stu-id="737a6-114">-Context</span></span>
<span data-ttu-id="737a6-115">Объект **AzureStorageContext** для текущей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="737a6-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="737a6-116">Чтобы получить объект контекстного хранилища, используйте New-AzStorageContext управления.</span><span class="sxs-lookup"><span data-stu-id="737a6-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="737a6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737a6-117">-DefaultProfile</span></span>
<span data-ttu-id="737a6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="737a6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737a6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="737a6-119">-Name</span></span>
<span data-ttu-id="737a6-120">Имя учетной записи хранения, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="737a6-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="737a6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737a6-121">-ResourceGroupName</span></span>
<span data-ttu-id="737a6-122">Указывает группу ресурсов, которая содержит изменяемую учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="737a6-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="737a6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737a6-123">CommonParameters</span></span>
<span data-ttu-id="737a6-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737a6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737a6-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="737a6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737a6-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="737a6-126">INPUTS</span></span>

### <span data-ttu-id="737a6-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="737a6-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="737a6-128">System.String</span><span class="sxs-lookup"><span data-stu-id="737a6-128">System.String</span></span>

## <span data-ttu-id="737a6-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="737a6-129">OUTPUTS</span></span>

### <span data-ttu-id="737a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="737a6-130">System.String</span></span>

## <span data-ttu-id="737a6-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="737a6-131">NOTES</span></span>

## <span data-ttu-id="737a6-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="737a6-132">RELATED LINKS</span></span>

[<span data-ttu-id="737a6-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="737a6-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


