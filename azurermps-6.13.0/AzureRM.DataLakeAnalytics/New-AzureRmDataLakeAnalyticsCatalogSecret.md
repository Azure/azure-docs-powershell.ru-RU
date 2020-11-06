---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticscatalogsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: ce6bd748a639116f1f6d2e5c42e824fb3687bdfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567766"
---
# <span data-ttu-id="c8be1-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="c8be1-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="c8be1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c8be1-102">SYNOPSIS</span></span>
<span data-ttu-id="c8be1-103">Создание секрета для каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8be1-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8be1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c8be1-104">SYNTAX</span></span>

### <span data-ttu-id="c8be1-105">CreateByFullURI</span><span class="sxs-lookup"><span data-stu-id="c8be1-105">CreateByFullURI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c8be1-106">CreateByHostNameAndPort</span><span class="sxs-lookup"><span data-stu-id="c8be1-106">CreateByHostNameAndPort</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8be1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8be1-107">DESCRIPTION</span></span>
<span data-ttu-id="c8be1-108">Командлет **New-AzureRmDataLakeAnalyticsCatalogSecret** создает секретный ключ для использования в каталоге Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8be1-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="c8be1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c8be1-109">EXAMPLES</span></span>

### <span data-ttu-id="c8be1-110">Пример 1: получение секрета для каталога</span><span class="sxs-lookup"><span data-stu-id="c8be1-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="c8be1-111">Эта команда возвращает секрет, соответствующий указанной учетной записи, базе данных, учетным данным и узлу.</span><span class="sxs-lookup"><span data-stu-id="c8be1-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="c8be1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c8be1-112">PARAMETERS</span></span>

### <span data-ttu-id="c8be1-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c8be1-113">-Account</span></span>
<span data-ttu-id="c8be1-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8be1-114">Specifies the name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="c8be1-115">-DatabaseHost</span></span>
<span data-ttu-id="c8be1-116">Указывает имя узла для базы данных, с которым связан секрет в формате "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="c8be1-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByFullURI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c8be1-117">-DatabaseName</span></span>
<span data-ttu-id="c8be1-118">Указывает имя базы данных, в которой хранится секрет.</span><span class="sxs-lookup"><span data-stu-id="c8be1-118">Specifies the name of the database that holds the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8be1-119">-DefaultProfile</span></span>
<span data-ttu-id="c8be1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c8be1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8be1-121">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="c8be1-121">-Port</span></span>
<span data-ttu-id="c8be1-122">Задает номер порта секрета.</span><span class="sxs-lookup"><span data-stu-id="c8be1-122">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateByFullURI
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-123">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="c8be1-123">-Secret</span></span>
<span data-ttu-id="c8be1-124">Указывает имя и пароль секрета.</span><span class="sxs-lookup"><span data-stu-id="c8be1-124">Specifies the name and password of the secret.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-125">-URI</span><span class="sxs-lookup"><span data-stu-id="c8be1-125">-Uri</span></span>
<span data-ttu-id="c8be1-126">Задает универсальный код ресурса (URI) секрета.</span><span class="sxs-lookup"><span data-stu-id="c8be1-126">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: CreateByHostNameAndPort
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8be1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8be1-127">CommonParameters</span></span>
<span data-ttu-id="c8be1-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c8be1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8be1-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8be1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8be1-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c8be1-130">INPUTS</span></span>

### <span data-ttu-id="c8be1-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c8be1-131">System.String</span></span>

### <span data-ttu-id="c8be1-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="c8be1-132">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="c8be1-133">System. URI</span><span class="sxs-lookup"><span data-stu-id="c8be1-133">System.Uri</span></span>

### <span data-ttu-id="c8be1-134">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c8be1-134">System.Int32</span></span>

## <span data-ttu-id="c8be1-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c8be1-135">OUTPUTS</span></span>

### <span data-ttu-id="c8be1-136">Microsoft. Azure. Management. данных Lake. Analytics. Models. USqlSecret</span><span class="sxs-lookup"><span data-stu-id="c8be1-136">Microsoft.Azure.Management.DataLake.Analytics.Models.USqlSecret</span></span>

## <span data-ttu-id="c8be1-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c8be1-137">NOTES</span></span>

## <span data-ttu-id="c8be1-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c8be1-138">RELATED LINKS</span></span>

[<span data-ttu-id="c8be1-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="c8be1-139">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="c8be1-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="c8be1-140">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


