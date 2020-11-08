---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAC3DABB-8230-4E86-9936-0F1848980EA2
online version: ''
schema: 2.0.0
ms.openlocfilehash: d062b4300af2efbd45bfccd7ed467871b23d8256
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076544"
---
# <span data-ttu-id="d6e84-101">Get-AzureVMAvailableExtension</span><span class="sxs-lookup"><span data-stu-id="d6e84-101">Get-AzureVMAvailableExtension</span></span>

## <span data-ttu-id="d6e84-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d6e84-102">SYNOPSIS</span></span>
<span data-ttu-id="d6e84-103">Получает сведения о последних доступных расширениях для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d6e84-103">Gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="d6e84-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d6e84-104">SYNTAX</span></span>

### <span data-ttu-id="d6e84-105">ListLatestExtensions (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d6e84-105">ListLatestExtensions (Default)</span></span>
```
Get-AzureVMAvailableExtension [[-ExtensionName] <String>] [[-Publisher] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="d6e84-106">ListAllVersions</span><span class="sxs-lookup"><span data-stu-id="d6e84-106">ListAllVersions</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-AllVersions]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="d6e84-107">ListSingleVersion</span><span class="sxs-lookup"><span data-stu-id="d6e84-107">ListSingleVersion</span></span>
```
Get-AzureVMAvailableExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d6e84-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6e84-108">DESCRIPTION</span></span>
<span data-ttu-id="d6e84-109">Командлет **Get-AzureVMAvailableExtension** получает сведения о последних доступных расширениях для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d6e84-109">The **Get-AzureVMAvailableExtension** cmdlet gets information for the latest available extensions for virtual machines.</span></span>

## <span data-ttu-id="d6e84-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d6e84-110">EXAMPLES</span></span>

### <span data-ttu-id="d6e84-111">Пример 1: получение сведений о последних доступных расширениях</span><span class="sxs-lookup"><span data-stu-id="d6e84-111">Example 1: Get information for the latest available extensions</span></span>
```
PS C:\> Get-AzureVMAvailableExtension
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d6e84-112">Эта команда получает сведения о последних доступных расширениях для всех виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d6e84-112">This command gets information for the latest available extensions for all virtual machines.</span></span>

### <span data-ttu-id="d6e84-113">Пример 2: получение сведений из указанного имени расширения</span><span class="sxs-lookup"><span data-stu-id="d6e84-113">Example 2: Get information from a specified extension name</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName "VMAccessAgent" -AllVersions
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.2
          PublicConfigurationSchema  : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          PrivateConfigurationSchema : 
          <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>

          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded

          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d6e84-114">Эта команда получает сведения из всех версий расширения с именем VMAccessAgent и издателя с именем Microsoft. Computer.</span><span class="sxs-lookup"><span data-stu-id="d6e84-114">This command gets information from all versions of the extension named VMAccessAgent and the publisher named Microsoft.Computer.</span></span>

### <span data-ttu-id="d6e84-115">Пример 3: получение сведений с определенного расширения виртуальной машины по номеру версии</span><span class="sxs-lookup"><span data-stu-id="d6e84-115">Example 3: Get information from a specific virtual machine extension by version number</span></span>
```
PS C:\> Get-AzureVMAvailableExtension -Publisher Microsoft.Compute -ExtensionName VMAccessAgent -Version 1.0.3
          Publisher                  : Microsoft.Compute
          ExtensionName              : VMAccessAgent
          Version                    : 1.0.3
          PublicConfigurationSchema  : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PublicConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="UserName" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          PrivateConfigurationSchema : <?xml version="1.0" encoding="utf-8"?>
          <xs:schema attributeFormDefault="unqualified" elementFormDefault="qualified"
          xmlns:xs="http://www.w3.org/2001/XMLSchema">
          <xs:element name="PrivateConfig">
          <xs:complexType>
          <xs:sequence>
          <xs:element name="Password" type="xs:string" minOccurs="0" />
          </xs:sequence>
          </xs:complexType>
          </xs:element>
          </xs:schema>
          SampleConfig               : 
          OperationDescription       : Get-AzureVMAvailableExtension
          OperationId                : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
          OperationStatus            : Succeeded
```

<span data-ttu-id="d6e84-116">Эта команда получает сведения о расширении с именем VMAccessAgent и издателе с именем Microsoft. COMPUTE для расширения версии 1.0.3.</span><span class="sxs-lookup"><span data-stu-id="d6e84-116">This command gets information for the extension named VMAccessAgent and the publisher named Microsoft.Compute for the extension version 1.0.3.</span></span>

## <span data-ttu-id="d6e84-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d6e84-117">PARAMETERS</span></span>

### <span data-ttu-id="d6e84-118">-AllVersions</span><span class="sxs-lookup"><span data-stu-id="d6e84-118">-AllVersions</span></span>
<span data-ttu-id="d6e84-119">Указывает на то, что этот командлет перечисляет все версии расширения.</span><span class="sxs-lookup"><span data-stu-id="d6e84-119">Indicates that this cmdlet lists all versions of an extension.</span></span>

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

### <span data-ttu-id="d6e84-120">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="d6e84-120">-ExtensionName</span></span>
<span data-ttu-id="d6e84-121">Указывает имя доступного расширения.</span><span class="sxs-lookup"><span data-stu-id="d6e84-121">Specifies the name of the available extension.</span></span>

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

### <span data-ttu-id="d6e84-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d6e84-122">-InformationAction</span></span>
<span data-ttu-id="d6e84-123">Указывает, как этот командлет отвечает на информационное событие.</span><span class="sxs-lookup"><span data-stu-id="d6e84-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d6e84-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="d6e84-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d6e84-125">Продолжал</span><span class="sxs-lookup"><span data-stu-id="d6e84-125">Continue</span></span>
- <span data-ttu-id="d6e84-126">Игнорируйте</span><span class="sxs-lookup"><span data-stu-id="d6e84-126">Ignore</span></span>
- <span data-ttu-id="d6e84-127">INQUIRE</span><span class="sxs-lookup"><span data-stu-id="d6e84-127">Inquire</span></span>
- <span data-ttu-id="d6e84-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d6e84-128">SilentlyContinue</span></span>
- <span data-ttu-id="d6e84-129">Остановить</span><span class="sxs-lookup"><span data-stu-id="d6e84-129">Stop</span></span>
- <span data-ttu-id="d6e84-130">Рвать</span><span class="sxs-lookup"><span data-stu-id="d6e84-130">Suspend</span></span>

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

### <span data-ttu-id="d6e84-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d6e84-131">-InformationVariable</span></span>
<span data-ttu-id="d6e84-132">Указывает переменную данных.</span><span class="sxs-lookup"><span data-stu-id="d6e84-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d6e84-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="d6e84-133">-Profile</span></span>
<span data-ttu-id="d6e84-134">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d6e84-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d6e84-135">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d6e84-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d6e84-136">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d6e84-136">-Publisher</span></span>
<span data-ttu-id="d6e84-137">Указывает издателя расширения.</span><span class="sxs-lookup"><span data-stu-id="d6e84-137">Specifies the publisher of the extension.</span></span>

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

### <span data-ttu-id="d6e84-138">-Version</span><span class="sxs-lookup"><span data-stu-id="d6e84-138">-Version</span></span>
<span data-ttu-id="d6e84-139">Указывает версию расширения.</span><span class="sxs-lookup"><span data-stu-id="d6e84-139">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="d6e84-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6e84-140">CommonParameters</span></span>
<span data-ttu-id="d6e84-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d6e84-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6e84-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6e84-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6e84-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d6e84-143">INPUTS</span></span>

## <span data-ttu-id="d6e84-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d6e84-144">OUTPUTS</span></span>

## <span data-ttu-id="d6e84-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="d6e84-145">NOTES</span></span>

## <span data-ttu-id="d6e84-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d6e84-146">RELATED LINKS</span></span>

