---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 2021B6BC-7B59-4A88-B1DF-598203F58901
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e225702238f9a90891db819753a68f728a482f9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075996"
---
# <span data-ttu-id="48897-101">New-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48897-101">New-AzureRemoteAppCollection</span></span>

## <span data-ttu-id="48897-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48897-102">SYNOPSIS</span></span>
<span data-ttu-id="48897-103">Создает коллекцию RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="48897-103">Creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="48897-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48897-104">SYNTAX</span></span>

### <span data-ttu-id="48897-105">AllParameterSets (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="48897-105">AllParameterSets (Default)</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-Description <String>] [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="48897-106">AzureVNet</span><span class="sxs-lookup"><span data-stu-id="48897-106">AzureVNet</span></span>
```
New-AzureRemoteAppCollection [-CollectionName] <String> [-ImageName] <String> [-Plan] <String>
 [[-Location] <String>] [-VNetName] <String> [-SubnetName] <String> [-DnsServers <String>] [[-Domain] <String>]
 [[-Credential] <PSCredential>] [-OrganizationalUnit <String>] [-Description <String>]
 [-CustomRdpProperty <String>] [-ResourceType <CollectionMode>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="48897-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48897-107">DESCRIPTION</span></span>
<span data-ttu-id="48897-108">Командлет **New-AzureRemoteAppCollection** создает коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="48897-108">The **New-AzureRemoteAppCollection** cmdlet creates an Azure RemoteApp collection.</span></span>

## <span data-ttu-id="48897-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48897-109">EXAMPLES</span></span>

### <span data-ttu-id="48897-110">Пример 1: создание коллекции</span><span class="sxs-lookup"><span data-stu-id="48897-110">Example 1: Create a collection</span></span>
```
PS C:\> New-AzureRemoteAppCollection -CollectionName "Contoso" -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
```

<span data-ttu-id="48897-111">Эта команда создает коллекцию Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="48897-111">This command creates an Azure RemoteApp collection.</span></span>

### <span data-ttu-id="48897-112">Пример 2: создание коллекции с помощью учетных данных</span><span class="sxs-lookup"><span data-stu-id="48897-112">Example 2: Create a collection using credentials</span></span>
```
PS C:\> $cred = Get-Credential corp.contoso.com\admin
PS C:\> New-AzureRemoteAppCollection -CollectionName "ContosoHybrid" -ImageName "Windows Server 2012 R2" -Plan Standard -VNetName azureVNet -Domain Contoso.com -Credential $cred -Description Hybrid
```

<span data-ttu-id="48897-113">Эта команда создает коллекцию Azure RemoteApp с учетными данными из командлета **Get-credentials** .</span><span class="sxs-lookup"><span data-stu-id="48897-113">This command creates an Azure RemoteApp collection using a credential from the **Get-Credential** cmdlet.</span></span>

## <span data-ttu-id="48897-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48897-114">PARAMETERS</span></span>

### <span data-ttu-id="48897-115">-CollectionName</span><span class="sxs-lookup"><span data-stu-id="48897-115">-CollectionName</span></span>
<span data-ttu-id="48897-116">Указывает имя коллекции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="48897-116">Specifies the name of the Azure RemoteApp collection.</span></span>

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

### <span data-ttu-id="48897-117">-Credential</span><span class="sxs-lookup"><span data-stu-id="48897-117">-Credential</span></span>
<span data-ttu-id="48897-118">Указывает учетные данные учетной записи службы, которая имеет разрешение на присоединение к домену серверов RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="48897-118">Specifies the credentials of a service account that has permission to join the Azure RemoteApp servers to your domain.</span></span>
<span data-ttu-id="48897-119">Чтобы получить объект **PSCredential** , используйте командлет **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="48897-119">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-120">-CustomRdpProperty</span><span class="sxs-lookup"><span data-stu-id="48897-120">-CustomRdpProperty</span></span>
<span data-ttu-id="48897-121">Определяет пользовательские свойства Protocal для удаленных рабочих столов (RDP), которые можно использовать для настройки перенаправления дисков и других параметров.</span><span class="sxs-lookup"><span data-stu-id="48897-121">Specifies custom Remote Desktop Protocal (RDP) properties which can be used to configure drive redirection and other settings.</span></span>
<span data-ttu-id="48897-122">Подробные сведения об этом приведены [в разделе параметры RDP служб удаленных рабочих столов на сервере Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx) `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` .  </span><span class="sxs-lookup"><span data-stu-id="48897-122">See [RDP Settings for Remote Desktop Services in Windows Server](https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)  `(https://technet.microsoft.com/library/ff393699(v=ws.10).aspx)` for details.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-123">-Описание</span><span class="sxs-lookup"><span data-stu-id="48897-123">-Description</span></span>
<span data-ttu-id="48897-124">Задает краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="48897-124">Specifies a short description for the object.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-125">-DnsServers</span><span class="sxs-lookup"><span data-stu-id="48897-125">-DnsServers</span></span>
<span data-ttu-id="48897-126">Задает разделенный запятыми список адресов IPv4 DNS-серверов.</span><span class="sxs-lookup"><span data-stu-id="48897-126">Specifies a comma-separated list of IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-127">-Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="48897-127">-Domain</span></span>
<span data-ttu-id="48897-128">Указывает имя домена доменных служб Active Directory, к которому нужно присоединиться к серверам узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="48897-128">Specifies the name of the Active Directory Domain Services domain to which to join the RD Session Host servers.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-129">-ImageName</span><span class="sxs-lookup"><span data-stu-id="48897-129">-ImageName</span></span>
<span data-ttu-id="48897-130">Указывает имя образа шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="48897-130">Specifies the name of the Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-131">-Location</span><span class="sxs-lookup"><span data-stu-id="48897-131">-Location</span></span>
<span data-ttu-id="48897-132">Указывает регион Azure коллекции.</span><span class="sxs-lookup"><span data-stu-id="48897-132">Specifies the Azure region of the collection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-133">-OrganizationalUnit</span><span class="sxs-lookup"><span data-stu-id="48897-133">-OrganizationalUnit</span></span>
<span data-ttu-id="48897-134">Указывает имя подразделения (OU), к которому нужно присоединиться к серверам узла сеансов удаленных рабочих столов, например OU = MyOu, DC = MyDomain, DC = ParentDomain, DC = com.</span><span class="sxs-lookup"><span data-stu-id="48897-134">Specifies the name of the organizational unit (OU) to which to join the RD Session Host servers, for example, OU=MyOu,DC=MyDomain,DC=ParentDomain,DC=com.</span></span>
<span data-ttu-id="48897-135">Атрибуты OU и DC должны вводиться прописными буквами.</span><span class="sxs-lookup"><span data-stu-id="48897-135">Attributes such as OU and DC must be in uppercase.</span></span>
<span data-ttu-id="48897-136">После создания коллекции подразделение не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="48897-136">The OU cannot be changed after the collection has been created.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-137">-Планирование</span><span class="sxs-lookup"><span data-stu-id="48897-137">-Plan</span></span>
<span data-ttu-id="48897-138">Указывает план коллекции RemoteApp Azure, который может определять ограничения на использование.</span><span class="sxs-lookup"><span data-stu-id="48897-138">Specifies the plan for the Azure RemoteApp collection, which may define the usage limits.</span></span>
<span data-ttu-id="48897-139">Используйте **Get-AzureRemoteAppPlan** , чтобы просмотреть доступные планы.</span><span class="sxs-lookup"><span data-stu-id="48897-139">Use **Get-AzureRemoteAppPlan** to see the plans available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-140">-Profile</span><span class="sxs-lookup"><span data-stu-id="48897-140">-Profile</span></span>
<span data-ttu-id="48897-141">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="48897-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="48897-142">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="48897-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="48897-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="48897-143">-ResourceType</span></span>
<span data-ttu-id="48897-144">Указывает тип ресурса коллекции.</span><span class="sxs-lookup"><span data-stu-id="48897-144">Specifies the resource type of the collection.</span></span>
<span data-ttu-id="48897-145">Допустимые значения этого параметра: "приложение" или "Рабочий стол".</span><span class="sxs-lookup"><span data-stu-id="48897-145">The acceptable values for this parameter are: App or Desktop.</span></span>

```yaml
Type: CollectionMode
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-146">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="48897-146">-SubnetName</span></span>
<span data-ttu-id="48897-147">Указывает имя подсети в виртуальной сети, используемой для создания коллекции RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="48897-147">Specifies the name of the subnet in the virtual network to use to create the Azure RemoteApp collection.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-148">-VNetName</span><span class="sxs-lookup"><span data-stu-id="48897-148">-VNetName</span></span>
<span data-ttu-id="48897-149">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="48897-149">Specifies the name of an Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: AzureVNet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48897-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48897-150">CommonParameters</span></span>
<span data-ttu-id="48897-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48897-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48897-152">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48897-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48897-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48897-153">INPUTS</span></span>

## <span data-ttu-id="48897-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48897-154">OUTPUTS</span></span>

## <span data-ttu-id="48897-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="48897-155">NOTES</span></span>

## <span data-ttu-id="48897-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48897-156">RELATED LINKS</span></span>

[<span data-ttu-id="48897-157">Get-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48897-157">Get-AzureRemoteAppCollection</span></span>](./Get-AzureRemoteAppCollection.md)

[<span data-ttu-id="48897-158">Get-AzureRemoteAppPlan</span><span class="sxs-lookup"><span data-stu-id="48897-158">Get-AzureRemoteAppPlan</span></span>](./Get-AzureRemoteAppPlan.md)

[<span data-ttu-id="48897-159">Remove-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48897-159">Remove-AzureRemoteAppCollection</span></span>](./Remove-AzureRemoteAppCollection.md)

[<span data-ttu-id="48897-160">Set-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48897-160">Set-AzureRemoteAppCollection</span></span>](./Set-AzureRemoteAppCollection.md)

[<span data-ttu-id="48897-161">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="48897-161">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)


