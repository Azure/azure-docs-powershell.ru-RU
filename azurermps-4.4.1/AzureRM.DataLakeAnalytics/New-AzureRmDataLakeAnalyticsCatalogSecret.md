---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: C0BE6C8D-37F5-445F-AE15-2CD4F8D8E031
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: e36030cbe1ccfe78db625d9d4142de13ba2f54ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559863"
---
# <span data-ttu-id="32fbc-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="32fbc-101">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="32fbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="32fbc-102">SYNOPSIS</span></span>
<span data-ttu-id="32fbc-103">Создание секрета для каталога Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="32fbc-103">Creates a Data Lake Analytics catalog secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32fbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="32fbc-104">SYNTAX</span></span>

### <span data-ttu-id="32fbc-105">Укажите полный URI</span><span class="sxs-lookup"><span data-stu-id="32fbc-105">Specify full URI</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-DatabaseHost] <String> [-Port] <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32fbc-106">Укажите имя узла и порт</span><span class="sxs-lookup"><span data-stu-id="32fbc-106">Specify host name and port</span></span>
```
New-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [-Secret] <PSCredential>
 [-Uri] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32fbc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="32fbc-107">DESCRIPTION</span></span>
<span data-ttu-id="32fbc-108">Командлет **New-AzureRmDataLakeAnalyticsCatalogSecret** создает секретный ключ для использования в каталоге Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="32fbc-108">The **New-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet creates a secret to use in an Azure Data Lake Analytics catalog.</span></span>

## <span data-ttu-id="32fbc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="32fbc-109">EXAMPLES</span></span>

### <span data-ttu-id="32fbc-110">Пример 1: получение секрета для каталога</span><span class="sxs-lookup"><span data-stu-id="32fbc-110">Example 1: Get the secret for a catalog</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdlAccount" -DatabaseName "databaseName" -Secret (Get-Credential) -Host "https://example.contoso.com" -Port 8080
```

<span data-ttu-id="32fbc-111">Эта команда возвращает секрет, соответствующий указанной учетной записи, базе данных, учетным данным и узлу.</span><span class="sxs-lookup"><span data-stu-id="32fbc-111">This command gets the secret corresponding to the specified account, database, credential, and host.</span></span>

## <span data-ttu-id="32fbc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="32fbc-112">PARAMETERS</span></span>

### <span data-ttu-id="32fbc-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="32fbc-113">-Account</span></span>
<span data-ttu-id="32fbc-114">Указывает имя учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="32fbc-114">Specifies the name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="32fbc-115">-DatabaseHost</span><span class="sxs-lookup"><span data-stu-id="32fbc-115">-DatabaseHost</span></span>
<span data-ttu-id="32fbc-116">Указывает имя узла для базы данных, с которым связан секрет в формате "mydatabase.contoso.com".</span><span class="sxs-lookup"><span data-stu-id="32fbc-116">Specifies the host name for the database the secret is associated with in the format 'mydatabase.contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: Specify full URI
Aliases: Host

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fbc-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32fbc-117">-DatabaseName</span></span>
<span data-ttu-id="32fbc-118">Указывает имя базы данных, в которой хранится секрет.</span><span class="sxs-lookup"><span data-stu-id="32fbc-118">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="32fbc-119">-Port (порт)</span><span class="sxs-lookup"><span data-stu-id="32fbc-119">-Port</span></span>
<span data-ttu-id="32fbc-120">Задает номер порта секрета.</span><span class="sxs-lookup"><span data-stu-id="32fbc-120">Specifies the port number of the secret.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specify full URI
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fbc-121">-Secret (секретный)</span><span class="sxs-lookup"><span data-stu-id="32fbc-121">-Secret</span></span>
<span data-ttu-id="32fbc-122">Указывает имя и пароль секрета.</span><span class="sxs-lookup"><span data-stu-id="32fbc-122">Specifies the name and password of the secret.</span></span>

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

### <span data-ttu-id="32fbc-123">-URI</span><span class="sxs-lookup"><span data-stu-id="32fbc-123">-Uri</span></span>
<span data-ttu-id="32fbc-124">Задает универсальный код ресурса (URI) секрета.</span><span class="sxs-lookup"><span data-stu-id="32fbc-124">Specifies the Uniform Resource Identifier (URI) of the secret.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Specify host name and port
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32fbc-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32fbc-125">-DefaultProfile</span></span>
<span data-ttu-id="32fbc-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="32fbc-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32fbc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32fbc-127">CommonParameters</span></span>
<span data-ttu-id="32fbc-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="32fbc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32fbc-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32fbc-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32fbc-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="32fbc-130">INPUTS</span></span>

## <span data-ttu-id="32fbc-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="32fbc-131">OUTPUTS</span></span>

### <span data-ttu-id="32fbc-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="32fbc-132">None</span></span>

## <span data-ttu-id="32fbc-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="32fbc-133">NOTES</span></span>

## <span data-ttu-id="32fbc-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="32fbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="32fbc-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="32fbc-135">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Remove-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="32fbc-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="32fbc-136">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


