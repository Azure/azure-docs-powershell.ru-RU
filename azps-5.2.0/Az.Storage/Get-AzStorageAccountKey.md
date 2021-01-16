---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325082"
---
# <span data-ttu-id="88654-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="88654-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="88654-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88654-102">SYNOPSIS</span></span>
<span data-ttu-id="88654-103">Ключи доступа для учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="88654-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="88654-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="88654-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88654-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="88654-105">DESCRIPTION</span></span>
<span data-ttu-id="88654-106">Для учетной записи хранилища Azure ключи доступа получаются с использованием cmdlet **Get-AzStorageAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="88654-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="88654-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="88654-107">EXAMPLES</span></span>

### <span data-ttu-id="88654-108">Пример 1. Получите ключи доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="88654-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="88654-109">Эта команда получает ключи для указанной учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="88654-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="88654-110">Пример 2. Получите определенный ключ доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="88654-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="88654-111">Пример 3. Список ключей доступа для учетной записи хранения, включая ключи Kerberos (если включена активная каталог)</span><span class="sxs-lookup"><span data-stu-id="88654-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="88654-112">Эта команда получает ключи для указанной учетной записи хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="88654-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="88654-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88654-113">PARAMETERS</span></span>

### <span data-ttu-id="88654-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88654-114">-DefaultProfile</span></span>
<span data-ttu-id="88654-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="88654-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88654-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="88654-116">-ListKerbKey</span></span>
<span data-ttu-id="88654-117">Список ключей Kerberos (если включена активная каталог) для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="88654-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="88654-118">Ключ Kerberos создается на учетную запись хранилища для проверки подлинности на основе удостоверений Azure с помощью доменной службы Azure Active Directory (Azure AD DS) или доменной службы Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="88654-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="88654-119">Он используется в качестве пароля удостоверения, зарегистрированного в службе доменов, представляют учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="88654-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="88654-120">Ключ Kerberos не предоставляет разрешения на выполнение любых операций управления или обработки данных в самолете с учетной записью хранилища.</span><span class="sxs-lookup"><span data-stu-id="88654-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88654-121">-Name</span><span class="sxs-lookup"><span data-stu-id="88654-121">-Name</span></span>
<span data-ttu-id="88654-122">Указывает имя учетной записи хранения, для которой этот cmdlet получает ключи.</span><span class="sxs-lookup"><span data-stu-id="88654-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="88654-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88654-123">-ResourceGroupName</span></span>
<span data-ttu-id="88654-124">Имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="88654-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="88654-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88654-125">CommonParameters</span></span>
<span data-ttu-id="88654-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88654-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88654-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88654-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88654-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="88654-128">INPUTS</span></span>

### <span data-ttu-id="88654-129">System.String</span><span class="sxs-lookup"><span data-stu-id="88654-129">System.String</span></span>

## <span data-ttu-id="88654-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="88654-130">OUTPUTS</span></span>

### <span data-ttu-id="88654-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="88654-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="88654-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="88654-132">NOTES</span></span>

## <span data-ttu-id="88654-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="88654-133">RELATED LINKS</span></span>

[<span data-ttu-id="88654-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="88654-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


