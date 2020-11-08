---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249762"
---
# <span data-ttu-id="0a5e5-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a5e5-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="0a5e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a5e5-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5e5-103">Получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="0a5e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a5e5-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a5e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5e5-105">DESCRIPTION</span></span>
<span data-ttu-id="0a5e5-106">Командлет **Get-AzStorageAccountKey** получает ключи доступа для учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="0a5e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a5e5-107">EXAMPLES</span></span>

### <span data-ttu-id="0a5e5-108">Пример 1: получение клавиш доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0a5e5-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="0a5e5-109">Эта команда получает ключи для указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="0a5e5-110">Пример 2: получение определенного ключа доступа для учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="0a5e5-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="0a5e5-111">Пример 3: список клавиш доступа для учетной записи хранения, включая ключи Kerberos (если включена служба каталогов Active Directory).</span><span class="sxs-lookup"><span data-stu-id="0a5e5-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="0a5e5-112">Эта команда получает ключи для указанной учетной записи хранения Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="0a5e5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a5e5-113">PARAMETERS</span></span>

### <span data-ttu-id="0a5e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5e5-114">-DefaultProfile</span></span>
<span data-ttu-id="0a5e5-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5e5-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="0a5e5-116">-ListKerbKey</span></span>
<span data-ttu-id="0a5e5-117">Список ключей Kerberos (если включена служба каталогов Active Directory) для указанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="0a5e5-118">Ключ Kerberos создается для учетной записи хранения для проверки подлинности на основе удостоверения файлов Azure либо службой доменных служб Active Directory (Azure AD DS), либо доменной службой Active Directory (AD DS).</span><span class="sxs-lookup"><span data-stu-id="0a5e5-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="0a5e5-119">Он используется в качестве пароля удостоверения, зарегистрированного в службе домена, которая представляет учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="0a5e5-120">Ключ Kerberos не предоставляет разрешения на доступ к операциям чтения или записи данных в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="0a5e5-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a5e5-121">-Name</span></span>
<span data-ttu-id="0a5e5-122">Указывает имя учетной записи хранилища, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="0a5e5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5e5-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a5e5-124">Указывает имя группы ресурсов, которая содержит учетную запись хранения.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="0a5e5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5e5-125">CommonParameters</span></span>
<span data-ttu-id="0a5e5-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a5e5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5e5-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5e5-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5e5-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a5e5-128">INPUTS</span></span>

### <span data-ttu-id="0a5e5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0a5e5-129">System.String</span></span>

## <span data-ttu-id="0a5e5-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5e5-130">OUTPUTS</span></span>

### <span data-ttu-id="0a5e5-131">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a5e5-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="0a5e5-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a5e5-132">NOTES</span></span>

## <span data-ttu-id="0a5e5-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a5e5-133">RELATED LINKS</span></span>

[<span data-ttu-id="0a5e5-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0a5e5-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


