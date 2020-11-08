---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075703"
---
# <span data-ttu-id="6077b-101">Clear-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="6077b-101">Clear-AzureRemoteAppVmStaleAdObject</span></span>

## <span data-ttu-id="6077b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6077b-102">SYNOPSIS</span></span>
<span data-ttu-id="6077b-103">Удаление объектов из Azure Active Directory, связанных с виртуальными машинами RemoteApp Azure, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="6077b-103">Removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>

## <span data-ttu-id="6077b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6077b-104">SYNTAX</span></span>

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6077b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6077b-105">DESCRIPTION</span></span>
<span data-ttu-id="6077b-106">Командлет **clear-AzureRemoteAppVmStaleAdObject** удаляет объекты в службе Azure Active Directory, связанные с виртуальными машинами RemoteApp Azure, которые больше не существуют.</span><span class="sxs-lookup"><span data-stu-id="6077b-106">The **Clear-AzureRemoteAppVmStaleAdObject** cmdlet removes objects in Azure Active Directory that are associated with Azure RemoteApp virtual machines that no longer exist.</span></span>
<span data-ttu-id="6077b-107">Для удаления объектов Azure Active Directory необходимо использовать учетные данные, имеющие права.</span><span class="sxs-lookup"><span data-stu-id="6077b-107">You must use credentials that have rights to remove Azure Active Directory objects.</span></span>
<span data-ttu-id="6077b-108">Если вы задаете *подробный* общий параметр, этот командлет выводит имя каждого объекта, который он удаляет.</span><span class="sxs-lookup"><span data-stu-id="6077b-108">If you specify the *Verbose* common parameter, this cmdlet displays the name of each object that it deletes.</span></span>

## <span data-ttu-id="6077b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6077b-109">EXAMPLES</span></span>

### <span data-ttu-id="6077b-110">Пример 1: удаление устаревших объектов для коллекции</span><span class="sxs-lookup"><span data-stu-id="6077b-110">Example 1: Clear stale objects for a collection</span></span>
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

<span data-ttu-id="6077b-111">Первая команда запрашивает имя пользователя и пароль с помощью команды **Get-Credential**.</span><span class="sxs-lookup"><span data-stu-id="6077b-111">The first command prompts you for a user name and password by using **Get-Credential**.</span></span>
<span data-ttu-id="6077b-112">Команда сохраняет результаты в переменной $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="6077b-112">The command stores the results in the $AdminCredentials variable.</span></span>

<span data-ttu-id="6077b-113">Вторая команда очищает устаревшие объекты для коллекции с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="6077b-113">The second command clears the stale objects for the collection named Contoso.</span></span>
<span data-ttu-id="6077b-114">В команде используются учетные данные, хранящиеся в переменной $AdminCredentials.</span><span class="sxs-lookup"><span data-stu-id="6077b-114">The command uses the credentials stored in $AdminCredentials variable.</span></span>
<span data-ttu-id="6077b-115">Для успешного завершения команды эти учетные данные должны иметь соответствующие права.</span><span class="sxs-lookup"><span data-stu-id="6077b-115">In order for the command to succeed, those credentials must have appropriate rights.</span></span>

## <span data-ttu-id="6077b-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6077b-116">PARAMETERS</span></span>

### <span data-ttu-id="6077b-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="6077b-117">-CollectionName</span></span>
<span data-ttu-id="6077b-118">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="6077b-118">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="6077b-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="6077b-119">-Credential</span></span>
<span data-ttu-id="6077b-120">Указывает учетные данные с правами на выполнение этого действия.</span><span class="sxs-lookup"><span data-stu-id="6077b-120">Specifies a credential that has rights to perform this action.</span></span>
<span data-ttu-id="6077b-121">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="6077b-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="6077b-122">Если этот параметр не указан, этот командлет использует учетные данные текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="6077b-122">If you do not specify this parameter, this cmdlet uses the current user credentials.</span></span>

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

### <span data-ttu-id="6077b-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="6077b-123">-Profile</span></span>
<span data-ttu-id="6077b-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6077b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6077b-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6077b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="6077b-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6077b-126">-Confirm</span></span>
<span data-ttu-id="6077b-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6077b-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6077b-128">-WhatIf</span></span>
<span data-ttu-id="6077b-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6077b-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6077b-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6077b-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6077b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6077b-131">CommonParameters</span></span>
<span data-ttu-id="6077b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6077b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6077b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6077b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6077b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6077b-134">INPUTS</span></span>

## <span data-ttu-id="6077b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6077b-135">OUTPUTS</span></span>

## <span data-ttu-id="6077b-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6077b-136">NOTES</span></span>

## <span data-ttu-id="6077b-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6077b-137">RELATED LINKS</span></span>

[<span data-ttu-id="6077b-138">Get-AzureRemoteAppVmStaleAdObject</span><span class="sxs-lookup"><span data-stu-id="6077b-138">Get-AzureRemoteAppVmStaleAdObject</span></span>](./Get-AzureRemoteAppVmStaleAdObject.md)


