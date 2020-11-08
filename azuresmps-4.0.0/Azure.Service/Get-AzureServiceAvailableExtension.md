---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFB0000C-2EFF-4216-923B-55B0B07BFE60
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51ab7d137fbbac1925ae689a1dcb16c89b9b8000
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075606"
---
# <span data-ttu-id="fb486-101">Get-AzureServiceAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="fb486-101">Get-AzureServiceAvailableExtension</span></span>

## <span data-ttu-id="fb486-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb486-102">SYNOPSIS</span></span>
<span data-ttu-id="fb486-103">Возвращает сведения о доступных расширениях для размещенных служб.</span><span class="sxs-lookup"><span data-stu-id="fb486-103">Gets information about the available extensions for hosted services.</span></span>

## <span data-ttu-id="fb486-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb486-104">SYNTAX</span></span>

### <span data-ttu-id="fb486-105">ListLatestExtensions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb486-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureServiceAvailableExtension [[-ExtensionName] <String>] [[-ProviderNamespace] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb486-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="fb486-106">ListAllVersions</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb486-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="fb486-107">ListSingleVersion</span></span>
```
Get-AzureServiceAvailableExtension [-ExtensionName] <String> [-ProviderNamespace] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb486-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb486-108">DESCRIPTION</span></span>
<span data-ttu-id="fb486-109">Командлет **Get-AzureServiceAvailableExtension** получает сведения о последних доступных расширениях для размещенных служб.</span><span class="sxs-lookup"><span data-stu-id="fb486-109">The **Get-AzureServiceAvailableExtension** cmdlet gets information for the latest available extensions for hosted services.</span></span>

## <span data-ttu-id="fb486-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb486-110">EXAMPLES</span></span>

### <span data-ttu-id="fb486-111">Пример 1: получение доступных расширений</span><span class="sxs-lookup"><span data-stu-id="fb486-111">Example 1: Get available extensions</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fb486-112">Эта команда получает все доступные расширения.</span><span class="sxs-lookup"><span data-stu-id="fb486-112">This command gets all available extensions.</span></span>

### <span data-ttu-id="fb486-113">Пример 2: получение расширений в указанном пространстве имен</span><span class="sxs-lookup"><span data-stu-id="fb486-113">Example 2: Get extensions in a specified namespace</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -AllVersions

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fb486-114">Эта команда получает расширения с указанным именем в указанном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="fb486-114">This command gets the extensions with a specified name in a specified namespace.</span></span>

### <span data-ttu-id="fb486-115">Пример 3: получение определенной версии расширения</span><span class="sxs-lookup"><span data-stu-id="fb486-115">Example 3: Get a specific version of an extension</span></span>
```
PS C:\> Get-AzureServiceAvailableExtension -ProviderNamespace Microsoft.Windows.Azure.Extensions -ExtensionName "RDP" -Version 1.0.0.1

          ProviderNameSpace          : Microsoft.Windows.Azure.Extensions
          ExtensionName              : RDP
          Version                    : 1.0.0.1
          Label                      : Microsoft Azure Remote Desktop Extension
          Description                : Microsoft Azure Remote Desktop Extension
          HostingResources           : WebOrWorkerRole
          ThumbprintAlgorithm        : sha1
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PublicConfig"><xs:complexType><xs:sequence><xs:element
          name="UserName" type="xs:string" minOccurs="1" /><xs:element name="Expiration" type="xs:string" minOccurs="1"
          /></xs:sequence></xs:complexType></xs:element></xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?><xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema"><xs:element name="PrivateConfig"><xs:complexType><xs:sequence><xs:element
          name="Password" type="xs:string" /></xs:sequence></xs:complexType></xs:element></xs:schema>
          OperationDescription       : Get-AzureServiceAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="fb486-116">Эта команда получает сведения о конкретной версии расширения.</span><span class="sxs-lookup"><span data-stu-id="fb486-116">This command gets information about a specific version of an extension.</span></span>

## <span data-ttu-id="fb486-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb486-117">PARAMETERS</span></span>

### <span data-ttu-id="fb486-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="fb486-118">-AllVersions</span></span>
<span data-ttu-id="fb486-119">Указывает на то, что этот командлет получает все версии расширения.</span><span class="sxs-lookup"><span data-stu-id="fb486-119">Indicates that this cmdlet gets all versions of an extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ListAllVersions
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="fb486-120">-ExtensionName</span></span>
<span data-ttu-id="fb486-121">Задает имя расширения.</span><span class="sxs-lookup"><span data-stu-id="fb486-121">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="fb486-122">-InformationAction</span></span>
<span data-ttu-id="fb486-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="fb486-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fb486-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb486-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb486-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="fb486-125">Continue</span></span>
- <span data-ttu-id="fb486-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="fb486-126">Ignore</span></span>
- <span data-ttu-id="fb486-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="fb486-127">Inquire</span></span>
- <span data-ttu-id="fb486-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="fb486-128">SilentlyContinue</span></span>
- <span data-ttu-id="fb486-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="fb486-129">Stop</span></span>
- <span data-ttu-id="fb486-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="fb486-130">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="fb486-131">-InformationVariable</span></span>
<span data-ttu-id="fb486-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="fb486-132">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="fb486-133">-Profile</span></span>
<span data-ttu-id="fb486-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fb486-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fb486-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="fb486-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fb486-136">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="fb486-136">-ProviderNamespace</span></span>
<span data-ttu-id="fb486-137">Задает пространство имен поставщика расширений.</span><span class="sxs-lookup"><span data-stu-id="fb486-137">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: ListLatestExtensions
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ListAllVersions, ListSingleVersion
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-138">-Version</span><span class="sxs-lookup"><span data-stu-id="fb486-138">-Version</span></span>
<span data-ttu-id="fb486-139">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="fb486-139">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: ListSingleVersion
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb486-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb486-140">CommonParameters</span></span>
<span data-ttu-id="fb486-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb486-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb486-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb486-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb486-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb486-143">INPUTS</span></span>

## <span data-ttu-id="fb486-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb486-144">OUTPUTS</span></span>

## <span data-ttu-id="fb486-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb486-145">NOTES</span></span>

## <span data-ttu-id="fb486-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb486-146">RELATED LINKS</span></span>

[<span data-ttu-id="fb486-147">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="fb486-147">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)


