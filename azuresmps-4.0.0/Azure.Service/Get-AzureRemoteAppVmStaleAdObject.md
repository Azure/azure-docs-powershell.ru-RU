---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: EC6AB7E9-BC9F-4FA2-8172-144C9842D74C
online version: ''
schema: 2.0.0
ms.openlocfilehash: da7ed2c382bfcec8327b291c46a51699b77b9373
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075630"
---
# <span data-ttu-id="fbf4c-101">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="fbf4c-101">Get-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="fbf4c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fbf4c-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf4c-103">Возвращает объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-103">Gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="fbf4c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fbf4c-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fbf4c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf4c-105">DESCRIPTION</span></span>
<span data-ttu-id="fbf4c-106">Командлет **Get-AzureRemoteAppVmStaleAdObject** получает объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-106">The **Get-AzureRemoteAppVmStaleAdObject** cmdlet gets objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="fbf4c-107">Этот командлет выводит имя каждого объекта, который он получает.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-107">This cmdlet displays the name of each object that it gets.</span></span>

## <span data-ttu-id="fbf4c-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fbf4c-108">EXAMPLES</span></span>

### <span data-ttu-id="fbf4c-109">Пример 1: получение устаревших объектов для коллекции</span><span class="sxs-lookup"><span data-stu-id="fbf4c-109">Example 1: Get stale objects for a collection</span></span>
```
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso"
```

<span data-ttu-id="fbf4c-110">Эта вторая команда получает старые объекты для коллекции с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-110">This second command gets the stale objects for the collection named Contoso.</span></span>

## <span data-ttu-id="fbf4c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fbf4c-111">PARAMETERS</span></span>

### <span data-ttu-id="fbf4c-112">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="fbf4c-112">-CollectionName</span></span>
<span data-ttu-id="fbf4c-113">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-113">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbf4c-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="fbf4c-114">-Credential</span></span>
<span data-ttu-id="fbf4c-115">Указывает учетные данные с правами на выполнение этого действия.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-115">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="fbf4c-116">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="fbf4c-116">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="fbf4c-117">Если этот параметр не указан, этот командлет использует учетные данные текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-117">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf4c-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="fbf4c-118">-Profile</span></span>
<span data-ttu-id="fbf4c-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbf4c-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf4c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf4c-121">CommonParameters</span></span>
<span data-ttu-id="fbf4c-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fbf4c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf4c-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf4c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf4c-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fbf4c-124">INPUTS</span></span>

## <span data-ttu-id="fbf4c-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fbf4c-125">OUTPUTS</span></span>

### <span data-ttu-id="fbf4c-126">Подстрок</span><span class="sxs-lookup"><span data-stu-id="fbf4c-126">String</span></span>

## <span data-ttu-id="fbf4c-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fbf4c-127">NOTES</span></span>

## <span data-ttu-id="fbf4c-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fbf4c-128">RELATED LINKS</span></span>

[<span data-ttu-id="fbf4c-129">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="fbf4c-129">Clear-AzureRemoteAppVmStaleAdObject</span></span>](./Clear-AzureRemoteAppVmStaleAdObject.md)


