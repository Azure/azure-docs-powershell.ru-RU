---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 14B4050D-3597-4760-A152-82617B88078D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 291ea94bbdfff1da8d658074ebfb72df8943f0e8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076053"
---
# <span data-ttu-id="b5804-101">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b5804-101">Set-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="b5804-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b5804-102">SYNOPSIS</span></span>
<span data-ttu-id="b5804-103">Задает свойства коллекции RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b5804-103">Sets the properties of a RemoteApp collection.</span></span>

## <span data-ttu-id="b5804-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b5804-104">SYNTAX</span></span>

### <span data-ttu-id="b5804-105">DescriptionOnly (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b5804-105">DescriptionOnly (Default)</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Description <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5804-106">PlanOnly</span><span class="sxs-lookup"><span data-stu-id="b5804-106">PlanOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Plan <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5804-107">DomainJoined</span><span class="sxs-lookup"><span data-stu-id="b5804-107">DomainJoined</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5804-108">RdpPropertyOnly</span><span class="sxs-lookup"><span data-stu-id="b5804-108">RdpPropertyOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -CustomRdpProperty <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="b5804-109">AclLevelOnly</span><span class="sxs-lookup"><span data-stu-id="b5804-109">AclLevelOnly</span></span>
```
Set-AzureRemoteAppCollection [-CollectionName] <String> -AclLevel <CollectionAclLevel>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b5804-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5804-110">DESCRIPTION</span></span>
<span data-ttu-id="b5804-111">Командлет **Set-AzureRemoteAppCollection** задает свойства коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b5804-111">The **Set-AzureRemoteAppCollection** cmdlet sets the properties of an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="b5804-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b5804-112">EXAMPLES</span></span>

## <span data-ttu-id="b5804-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b5804-113">PARAMETERS</span></span>

### <span data-ttu-id="b5804-114">-AclLevel</span><span class="sxs-lookup"><span data-stu-id="b5804-114">-AclLevel</span></span>
<span data-ttu-id="b5804-115">Задает уровень списка управления доступом (ACL) для коллекции.</span><span class="sxs-lookup"><span data-stu-id="b5804-115">Specifies the access control list (ACL) level for the collection.</span></span>
<span data-ttu-id="b5804-116">Допустимые значения этого параметра: Collection и Application.</span><span class="sxs-lookup"><span data-stu-id="b5804-116">The acceptable values for this parameter are: Collection and Application.</span></span>

```yaml
Type: CollectionAclLevel
Parameter Sets: AclLevelOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-117">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="b5804-117">-CollectionName</span></span>
<span data-ttu-id="b5804-118">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="b5804-118">Specifies the name of the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="b5804-119">-Credential</span></span>
<span data-ttu-id="b5804-120">Указывает учетные данные учетной записи службы, которая имеет разрешение на присоединение к домену серверов RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="b5804-120">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="b5804-121">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="b5804-121">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: DomainJoined
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-122">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="b5804-122">-CustomRdpProperty</span></span>
<span data-ttu-id="b5804-123">Определяет пользовательские свойства протокола удаленного рабочего стола (RDP), которые можно использовать для настройки перенаправления дисков и других параметров.</span><span class="sxs-lookup"><span data-stu-id="b5804-123">Specifies custom Remote Desktop Protocol (RDP) properties which can be used to configure drive redirection and other settings.</span></span> <span data-ttu-id="b5804-124">Подробные сведения об этом приведены [в разделе параметры RDP служб удаленных рабочих столов на сервере Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="b5804-124">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: RdpPropertyOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-125">-Описание</span><span class="sxs-lookup"><span data-stu-id="b5804-125">-Description</span></span>
<span data-ttu-id="b5804-126">Задает краткое описание коллекции.</span><span class="sxs-lookup"><span data-stu-id="b5804-126">Specifies a short description for the collection.</span></span>

```yaml
Type: String
Parameter Sets: DescriptionOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-127">-Планирование</span><span class="sxs-lookup"><span data-stu-id="b5804-127">-Plan</span></span>
<span data-ttu-id="b5804-128">Указывает план коллекции Azure RemoteApp, который определяет ограничения на использование.</span><span class="sxs-lookup"><span data-stu-id="b5804-128">Specifies the plan for the Azure RemoteApp collection, which defines the usage limits.</span></span>
<span data-ttu-id="b5804-129">Используйте **Get-AzureRemoteAppPlan** , чтобы просмотреть доступные планы.</span><span class="sxs-lookup"><span data-stu-id="b5804-129">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: PlanOnly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5804-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="b5804-130">-Profile</span></span>
<span data-ttu-id="b5804-131">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b5804-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b5804-132">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b5804-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b5804-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5804-133">CommonParameters</span></span>
<span data-ttu-id="b5804-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b5804-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5804-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5804-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5804-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b5804-136">INPUTS</span></span>

## <span data-ttu-id="b5804-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b5804-137">OUTPUTS</span></span>

## <span data-ttu-id="b5804-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b5804-138">NOTES</span></span>

## <span data-ttu-id="b5804-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b5804-139">RELATED LINKS</span></span>

[<span data-ttu-id="b5804-140">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b5804-140">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="b5804-141">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b5804-141">New-AzureRemoteAppCollection</span></span>](./New-AzureRemoteAppCollection.md)

[<span data-ttu-id="b5804-142">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="b5804-142">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


